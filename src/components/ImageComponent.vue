<template>
    <div class="container mt-5">
        <div class="row g-3 align-items-center">
            <div class="col-auto">
                <label for="inputOperation" class="col-form-label"><strong>Iteration 3</strong></label>
            </div>

            <div v-if="isClicked" class="col-3">
                <img src="./../assets/dog.jpg" class="rounded mx-auto d-block" alt="Dog picture" />
            </div>

            <div class="col-1">
                <button @click="showImg()" type="button" class="btn btn-warning">{{ buttonName }}</button>
            </div>

            <div v-if="isClicked" class="col-2">
                <button @click="hideImg()" type="button" class="btn btn-danger">Hide :(</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isClicked: false,
            buttonName: 'Click'
        }
    },
    methods: {
        showImg() {
            this.isClicked = true
            this.buttonName = 'Hellow!'
        },
        hideImg() {
            this.isClicked = false
            this.buttonName = 'Click'
        }
    }
}
</script>

<style scoped>
img {
    width: 100%;
}
</style>