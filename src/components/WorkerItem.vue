<template>
  <div class="worker">
    <div>
      <div><strong>Имя:</strong>{{ worker.name }}</div>
      <div><strong>Возраст:</strong>{{ worker.age }}</div>
    </div>
    <div class="post__btns">
      <my-button @remove="$emit('remove', worker)">
        Удалить
      </my-button>
    </div>
  </div>
</template>

<script>
import MyButton from "@/components/UI/MyButton.vue";

export default {
  components: {MyButton},
  props: {
    worker: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.worker{
  padding: 15px;
  border: 2px dotted #cf5353;
  margin: 15px auto;
  max-width: 500px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>