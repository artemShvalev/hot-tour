<template>
  <transition name="modal-fade">
  <div class="modal-backdrop">
    <div class="modal">
      <slot name="header">
        С обработкой персональных данных:
        <hr>
        <button
          type="button"
          class="btn-close"
          @click="close"
        >
          Согласен <input class="input__agree" type="checkbox">
        </button>

        <button
          type="button"
          class="btn-close"
          @click="close"
        >
           Не согласен <input type="checkbox">
        </button>
      </slot>

      <slot name="footer">
        <slot name="footer">

          <button
            type="button"
            class="btn-green"
            @click="close"
          >
            Закрыть окно
          </button>
          </slot>
      </slot>
    </div>
  </div>
  </transition>
</template>

<script>
export default {
  name: '_ModalForm',
  methods: {
    close() {
      this.$emit('close');
    },
  },
};
</script>

<style scoped lang="scss">
  .modal-backdrop {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgba(0, 0, 0, 0.3);
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .modal {
    background: #FFFFFF;
    box-shadow: 2px 2px 20px 1px;
    overflow-x: auto;
    display: flex;
    flex-direction: column;
    font-family: "Roboto Light",sans-serif;
    font-size:16px;
    padding: 15px;
  }

  .modal-header,
  .modal-footer {
    padding: 15px;
    display: flex;
  }

  .modal-header {
    border-bottom: 1px solid #eeeeee;
    color: #dbca6e;
    justify-content: space-between;
  }

  .modal-footer {
    border-top: 1px solid #eeeeee;
    justify-content: flex-end;
  }

  .modal-body {
    position: relative;
    padding: 20px 10px;
  }

  .btn-close {
    border: none;
    font-size: 20px;
    padding: 20px;
    cursor: pointer;
    font-weight: bold;
    color: #000000;
    background: transparent;
  }

  .btn-green {
    color: white;
    background: #e5d475;
    border: 1px solid #ffffff;
    border-radius: 2px;
    height: 70px;
    text-align: center;
  }
  .modal-fade-enter,
  .modal-fade-leave-active {
    opacity: 0;
  }

  .modal-fade-enter-active,
  .modal-fade-leave-active {
    transition: opacity .5s ease
  }
  button{
    max-width: 100%;
  }
  input{
    width:40px;
    border-radius:3px ;
  }
  .input__agree{
    width:40px;
    border-radius:3px;
    margin-left:30px ;
  }
  @media (max-width: 375px) {
    .modal {
      background: #FFFFFF;
      overflow-x: auto;
      display: flex;
      flex-direction: column;
      font-family: "Roboto Light",sans-serif;
      font-size:16px;
      padding: 15px;
      position: absolute;
      top: 1500px;
      left:40px;
    }
  }
</style>
