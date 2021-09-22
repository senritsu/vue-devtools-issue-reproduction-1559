<template lang="html">
  Hello from {{ foo }} and {{ bar }} with generic props
</template>

<script lang="ts" setup>
import type { Foo } from "../types";

defineProps<{ foo: Foo[] | null; bar?: string }>();
</script>
