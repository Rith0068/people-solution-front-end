<template>
  <div class="flex justify-between items-start p-6 hover:bg-gray-50 transition">
    <div class="w-full">
      <p class="text-sm text-gray-500">{{ label }}</p>

      <div v-if="!editing" class="mt-1 flex justify-between items-center">
        <p class="font-semibold text-gray-800">
          {{ modelValue || 'Not provided' }}
        </p>

        <button
          @click="editing = true"
          class="text-indigo-600 text-sm font-medium hover:underline"
        >
          Edit
        </button>
      </div>

      <div v-else class="mt-3 flex gap-3">
        <input
          :type="type || 'text'"
          v-model="localValue"
          class="border rounded-lg px-3 py-2 w-full focus:ring-2 focus:ring-indigo-500 outline-none"
        />

        <button
          @click="save"
          class="bg-indigo-600 text-white px-4 rounded-lg"
        >
          Save
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  label: String,
  modelValue: String,
  type: String
})

const emit = defineEmits(['update:modelValue'])

const editing = ref(false)
const localValue = ref(props.modelValue)

watch(() => props.modelValue, (val) => {
  localValue.value = val
})

const save = () => {
  emit('update:modelValue', localValue.value)
  editing.value = false
}
</script>
