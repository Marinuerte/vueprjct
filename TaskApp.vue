<script>
import Tasks from './Tasks.vue'
export default {
  components: {
    Tasks
  },
  data() {
        return {
            tasks: [
                {
                date: '13.03.2024',
                numbers: ['1'],
                title: ' Задача',
                text: '',
                author: 'Лорум Ипсум',
                comments: [
                    'Недооценённый материал...',
                ],
                date: '13.03.2024',
                },
                {
                date: '13.03.2024',
                numbers: ['2'],
                title: ' Задача',
                text: '',
                author: 'Лорум Ипсум',
                comments: [
                    'Круто!!!',
                ],
                },
                {
                date: '13.03.2024',
                numbers: ['3'],
                title: ' Задача',
                text: '',
                author: 'Лорум Ипсум',
                comments: [
                    'Недооценённый материал...',
                ],
                },
                {
                date: '13.03.2024',
                numbers: ['4'],
                title: ' Задача',
                text: '',
                author: 'Лорум Ипсум',
                comments: [
                    'Лучшее, что я читал.',
                ],
                },
                {
                date: '13.03.2024',
                numbers: ['5'],
                title: ' Задача',
                text: '',
                author: 'Лорум Ипсум',
                comments: [
                    'Круто!!!',
                ],
                },
            ],
            fontSize: 19
          };
        },
    methods: {
        fontSizeIncrease() {
        this.fontSize++
        },

        fontSizeDecrease() {
        this.fontSize--
        },

        fontSizeSet(a) {
        this.fontSize = a
        },
    }
};
</script>

<template>
  <header class="mb-5">
    <nav class="navbar">
      <div class="container-fluid">
        <h1 class="navbar-brand text-white">Задачи:</h1>
      </div>
    </nav>
  </header>
  <main class="container">
    <div class="row g-2">
      <!-- Вывод всех задач -->
      <div class="col-12" v-for="task in tasks">
          <Tasks :task="task" :fontSize="fontSize" @fontSizeIncrease ="fontSizeIncrease" @fontSizeDecrease ="fontSizeDecrease" @fontSizeSet ="fontSizeSet"/>
      </div>
    </div>
  </main>
</template>

<style>

.navbar {
  background-color: rgba(95, 79, 79, 0.5);
  color: white;
  border-radius: 20px;
  padding: 5px;
  text-align: center;
}
</style>