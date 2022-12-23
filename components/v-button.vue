<template>
  <div
    :class="[
      'btn',
      color == 'primary' ? 'btn--primary' : '',
      color == 'secondary' ? 'btn--secondary' : '',
      hover == 'primary' ? 'btn--primary-hover' : '',
      hover == 'secondary' ? 'btn--secondary-hover' : '',
      type == 'centered' ? 'btn--centered' : '',
    ]"
  >
    <div class="btn-txt">
      {{ text }}
    </div>
    <div class="btn-icon">
      <svg-icon class="icon icon-font" :name="icon" />
    </div>
  </div>
</template>

<script>
export default {
  props: ["color", "icon", "hover", "text", "type"],
};
</script>
