<template>
  <div class="demo-fit">
    <el-avatar
      :size="size"
      :shape="shape"
      style="
        background: transparent;
        border: 1px solid var(--el-text-color-secondary);
      "
      :fit="fit"
      :src="src"
    />
  </div>
</template>
<script lang="ts" setup>
const props = defineProps({
  src: {
    type: String,
    required: true,
    default: 'https://www.adempiere.io/logo.svg',
  },
  fit: {
    type: String,
    default: 'cover',
  },
  size: {
    type: String || Number,
    default: '',
  },
  shape: {
    type: String,
    default: 'circle',
  },
});
</script>

<style scoped>
.demo-fit {
  display: flex;
  text-align: center;
  justify-content: space-between;
}
.demo-fit .block {
  flex: 1;
  display: flex;
  flex-direction: column;
  flex-grow: 0;
}

.demo-fit .title {
  margin-bottom: 10px;
  font-size: 14px;
  color: var(--el-text-color-secondary);
}
</style>
