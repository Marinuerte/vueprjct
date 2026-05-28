<script>
export default {
    props: {
        task: Object,
        fontSize: Number
    },
    data() {
        return {
            text: 'Я задача',
        }
    },
}
</script>
<template>
    <div class="card shadow-sm">
        <div class="card-body">
            <small class="text-body-secondary">{{ task.author }}</small>
            <h3 class="card-title" v-for="number in task.numbers">{{ number }}{{ task.title }}</h3>
            <p class="card-subtitle text-secondary">{{ task.date }}</p><br>
            <input :style="{'fontSize': fontSize + 'px'}" v-model="text">
            <h4>Комментарии:</h4>
            <ul class="list-group list-group-flush">
                <!-- Вывод всех комментарии -->
                <li class="list-group-item" v-for="comment in task.comments">{{ comment }}</li>
            </ul>
            <div class="d-flex justify-content-between align-items-center ">
                <div class="btn-group">
                    <div class="btn-group">
                        <button type="button" class="btn btn-sm btn-outline-secondary" @click="$emit('fontSizeDecrease')">-</button>
                        <button type="button" class="btn btn-sm btn-outline-secondary" @click="$emit('fontSizeIncrease')">+</button>
                        <button type="button" class="btn btn-sm btn-outline-secondary" @click="$emit('fontSizeSet', 20)">20px</button>
                    </div>
                    <!-- <input v-model="fontSizeNew" class="form-control ms-3" type="text" placeholder="px" style="width: 50px;">
                    <button type="button" class="btn btn-sm btn-outline-secondary">Установить</button> -->

                </div>
            </div>

            <hr>

        </div>
    </div>
</template>
<style>
input {
    background-color: rgba(0, 0, 0, 0);
    color: white;
    resize: none;
    border-color: rgba(0, 0, 0, 0);
    border-radius: 20px;
    padding-left: 6px;
    font-size: 10px;
}

.btn {
    background-color: rgba(095, 79, 79, 0.5);
    color: white;
    border: none;
    margin-right: 2px;
}
</style>