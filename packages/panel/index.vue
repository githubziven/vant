<template>
  <div class="van-panel van-hairline--top-bottom">
    <div class="van-panel__header van-hairline--bottom">
      <slot name="header">
        <div class="van-panel__title" v-text="title" />
        <span class="van-panel__desc" v-if="desc" v-text="desc" />
        <span class="van-panel__status" v-if="status" v-text="status" />
      </slot>
    </div>
    <div class="van-panel__content">
      <slot />
    </div>
    <div class="van-panel__footer van-hairline--top" v-if="$slots.footer">
      <slot name="footer" />
    </div>
  </div>
</template>

<script>
import create from '../utils/create';

export default create({
  name: 'panel',
  props: {
    desc: String,
    title: String,
    status: String
  }
});
</script>
