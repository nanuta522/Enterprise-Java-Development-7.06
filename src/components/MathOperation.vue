<template>
    <div class="container mt-5">
        <div class="row g-3 align-items-center">
            <div class="col-auto">
                <label for="inputOperation" class="col-form-label"><strong>Iteration 2.1</strong></label>
            </div>

            <div class="col-auto">
                <input v-model="input" name="input" type="text" id="input" class="form-control" placeholder="Math operation + - * /">
            </div>

            <div class="col-auto">
                <div class="btn-group" role="group">
                    <button @click="operationResult()" type="button"
                        class="btn btn-outline-secondary btn-light">Result</button>
                    <button type="button" class="btn btn-outline-secondary">{{ inputResult }}</button>
                </div>
            </div>
        </div>
    </div>

    <div class="container mt-5">
        <div class="row g-3 align-items-center">
            <div class="col-auto">
                <label for="sumResult" class="col-form-label"><strong>Iteration 2.2</strong></label>
            </div>

            <div class="col-auto">
                <div class="btn-group" role="group">
                    <button @click="sum()" type="button" class="btn btn-outline-secondary btn-light">Result</button>
                    <button type="button" class="btn btn-outline-secondary">{{ sumResult }}</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            input: '',
            inputResult: 0,
            sumResult: 0
        }
    },
    props: {
        numbers: {
            type: Array
        }
    },
    components: {
    },
    methods: {
        operationResult() {
            if (this.input !== '') this.inputResult = eval(this.input)
            else this.inputResult = 0
        },
        sum() {
            this.sumResult = this.numbers.reduce((acc, cur) => acc + cur, 0)
        }
    }
}
</script>

<style>

</style>