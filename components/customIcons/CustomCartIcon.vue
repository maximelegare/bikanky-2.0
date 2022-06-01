<template>
  <v-btn
    large
    icon
    class="btn"
    @click.stop="clipped = !clipped"
  >
    <v-icon class="cart" medium>mdi-cart</v-icon>
    <div class="circle">
      <h3>{{ cartItemCount }}</h3>
    </div>
  </v-btn>
</template>

<script>
export default {
  name: 'CustomCartIcon',
  props: {
    cartItemCount: {
      type: Number,
      default() {
        return 0
      },
    },
  },
}
</script>

<style lang="scss" scoped>
@import '../../assets/variables.scss';

.v-btn:hover {
  background-color: transparent !important; 
  .v-icon.cart {
    color: $accent-color;
  }
}
.btn {
  position: relative;
}

.circle {
  border-radius: 50%;
  background-color: $accent-color;
  color: black;
  position: absolute;
  width: 30px;
  height: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  left: 20px;
  top: -15px;
  box-shadow: $light-box-shadow;
  z-index: 100;
}
</style>
