<template>
  <div class="todo">
    <div><strong>Задача:</strong>{{ todo.title }}</div>
    <div class="post__btns">
      <my-button @remove="$emit('remove', todo)">
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
    todo: {
      type: Object,
      required: true,
    }
  }
}
</script>

<style scoped>
.todo{
  padding: 15px;
  border: 2px dotted #cf5353;
  margin: 15px auto;
  max-width: 500px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>