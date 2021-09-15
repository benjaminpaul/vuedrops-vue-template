<template>
  <div class="input-wrapper">
    <p
      class="placeholder"
      v-bind:class="{ moved: !showPlaceholder, invalidPlaceholder: !isValid }"
    >
      {{ placeholder }}
    </p>
    <input
      v-model="currentValue"
      autocomplete="off"
      class="text-input"
      id="text-input"
      @focus="onFocusChanged"
      @blur="onBlurChanged"
      v-bind:class="{ invalid: !isValid }"
    />
    <transition name="fade">
      <div v-show="!isValid" class="validation-errors">
        <p>
          <i class="fas fa-exclamation-circle"></i>&nbsp;{{
            currentValidationError
          }}
        </p>
      </div>
    </transition>
  </div>
</template>

<script>
import { ref, computed, watch } from "vue";
export default {
  setup(props) {
    const currentValue = ref("");
    const validationErrors = ref([]);
    const valueHasChanged = ref(false);
    const validate = () => {
      if (valueHasChanged.value) {
        validationErrors.value = [];
        if (currentValue.value.trim().length === 0) {
          validationErrors.value.push("This field is required");
        }
      }
    };
    const onFocusChanged = () => {
      if (props.validateOnFocus) {
        validate();
      }
    };
    const onBlurChanged = () => {
      if (props.validateOnBlur) {
        validate();
      }
    };
    const isValid = computed(() => {
      return validationErrors.value.length === 0;
    });
    const showPlaceholder = computed(() => {
      return currentValue.value.trim().length === 0;
    });
    const currentValidationError = computed(() => {
      return validationErrors.value[0];
    });
    watch(currentValue, (value, oldValue) => {
      if (value !== oldValue) {
        valueHasChanged.value = true;
      }
    });
    return {
      currentValue,
      valueHasChanged,
      validationErrors,
      isValid,
      showPlaceholder,
      currentValidationError,
      validate,
      onFocusChanged,
      onBlurChanged,
    };
  },
  props: {
    placeholder: {
      type: String,
      default: "",
      required: false,
    },
    validateOnFocus: {
      type: Boolean,
      default: false,
      required: false,
    },
    validateOnBlur: {
      type: Boolean,
      default: true,
      required: false,
    },
  },
};
</script>

<style lang="scss" scoped>
.input-wrapper {
  .text-input {
    @apply shadow appearance-none border rounded w-full py-5 px-3 text-gray-700 leading-tight;
  }
  .invalid {
    @apply border border-red-600;
  }
  .placeholder {
    @apply absolute pl-4 text-sm;
    margin-top: 20px;
    opacity: 0.3;
    transition: all 0.3s;
    overflow: hidden;
    pointer-events: none;
  }
  .moved {
    color: blue;
    margin-top: -32px;
    padding-left: 0;
    opacity: 1;
  }
  .validation-errors {
    p {
      @apply m-2 text-red-600;
    }
  }
}
</style>