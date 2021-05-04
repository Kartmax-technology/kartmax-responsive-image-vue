<template>
  <div>
    <picture>
      <source :srcset="largeScreen + this.environment + image.largeScreen" media="(min-width: 1440px)" />
      <source :srcset="desktop + this.environment + image.desktop" media="(min-width: 1025px)" />
      <source media="(min-width: 768px)" :srcset="tab +  this.environment + image.tab" />
      <source media="(min-width: 320px)" :srcset="mobile + this.environment + image.mobile" />
      <img
        class="img-responsive lazy padding-0 margin-0"
        :class="custom_class"
        :width="custom_width"
        id="veuLogo"
        :src="default_image"
        :srcset="default_image + this.environment + image.default_image"
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
    custom_width: "",
    custom_style: "",
    custom_class: "",
    data_src: "",
    image:Object
  },
  data: function () {
    return {
      environment : ''
    };
  },

  mounted(){
    this.environment = this.$root.image_change_url
  }
};
</script>

<style></style>
