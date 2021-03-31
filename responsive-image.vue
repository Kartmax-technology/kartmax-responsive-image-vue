<template>
  <div>
    <picture>
      <source :srcset="largeScreen" media="(min-width: 1440px)" />
      <source :srcset="desktop" media="(min-width: 1025px)"/>
      <source  media="(min-width: 768px)" :srcset="tab"/>
      <source media="(min-width: 320px)" :srcset="mobile"/>
      <img
          class="img-responsive lazy padding-0 margin-0" :class="custom_class" :width="custom_width"
          id="veuLogo"
          :src="default_image"
          :srcset="default_image"
          :style="custom_style"
          :data-src="data_src"
          alt="a head carved out of wood"
      />
    </picture>
  </div>
</template>

<script>
export default {
  props: {
    desktop: String,
    tab: String,
    mobile: String,
    default_image: String,
    largeScreen: String,
    custom_width:'',
    custom_style:'',
    custom_class:'',
    data_src:'',
  },
  data: function () {
    return {};
  },
 

};
</script>

<style></style>
