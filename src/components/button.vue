<template>
    <button :disabled="disabled"  :type="nativeType" class="mint-button"
    :class="['mint-button--' + type, 'mint-button--' + size, {
      'is-disabled': disabled,
      'is-plain': plain
    }]">
        <label class="mint-button-text"><slot></slot></label>
    </button>
</template>
<style lang="less">

.mint-button--primary{
   color: #fff;
    background-color: #26a2ff;
}
.mint-button--default {
    color: #656b79;
    background-color: #f6f8fa;
    box-shadow: 0 0 1px #b8bbbf;
}
.mint-button--normal, .mint-button--small {
    display: inline-block;
    padding: 0 12px;
}
.mint-button--danger {
    color: #fff;
    background-color: #ef4f4f;
  padding: 5px;
}
.mint-button--large{
    width: 100%;
     font-size: 14px;
    height: 50px;
}
.mint-button--small {
    font-size: 14px;
    height: 33px;
}

.mint-button-text{
    color: white;
}
.mint-button {
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;
    border-radius: 4px;
    border: 0;
    box-sizing: border-box;
    color: inherit;
    display: block;
    font-size: 18px;
    height: 41px;
    outline: 0;
    overflow: hidden;
    position: relative;
    text-align: center;
}
</style>

<script>
export default {
     name: 'mt-button',
    
    props: {
    disabled: Boolean,
    nativeType: String,
    plain: Boolean,
    type: {
      type: String,
      default: 'default',
      validator(value) {
        return [
          'default',
          'danger',
          'primary'
        ].indexOf(value) > -1;
      }
    },
    size: {
      type: String,
      default: 'normal',
      validator(value) {
        return [
          'small',
          'normal',
          'large'
        ].indexOf(value) > -1;
      }
    }
  }
}
</script>

