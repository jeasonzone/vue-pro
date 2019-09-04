<template>
  <div>
    <button style="padding: 20px" @click="open">打开对话框</button>
    <Modal
      title="对话框"
      v-model="modal"
      :maskClosable="false"
      :loading="modalLoading"
      @on-ok="ok"
      ref="modal"
    ></Modal>
  </div>
</template>
<script>
export default {
  data() {
    return {
      modal: false
    };
  },
  methods: {
    open() {
      this.modal = true;
    },
    ok() {
      this.$Message.info("点击了确定");
    }
  }
};
</script>
