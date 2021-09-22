<template lang="html">
  Hello from {{ foo }} and {{ bar }} with object props
</template>

<script lang="ts" setup>
import type { PropType } from "vue";
import type { Foo } from "../types";

defineProps({
  foo: { type: null as unknown as PropType<Foo[] | null>, required: true },
  bar: { type: String, default: "" },
});
</script>
