<template>
    <div class="container mt-5">
        <div class="row g-3">
            <div class="col-auto">
                <label for="inputOperation" class="col-form-label"><strong>Iteration 5</strong></label>
            </div>
            <div class="col-auto">
                <div :class="[btn=== 1 ? 'alert alert-success' : '', btn=== 2 ? 'alert alert-danger' : '',  btn=== 3 ? 'alert alert-warning' : '']">
                    <strong>I'm {{ activeColor }}!</strong> You can change the color clicking the button below.
                </div>
                <div class="row">
                    <div class="col-auto">
                        <button @click="select(1, $event)" type="button" class="btn btn-success">Green</button>
                    </div>

                    <div class="col-auto">
                        <button @click="select(2, $event)" type="button" class="btn btn-danger">Red</button>
                    </div>

                    <div class="col-auto">
                        <button @click="select(3, $event)" type="button" class="btn btn-warning">Yellow</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            activeColor: 'YELLOW',
            btn: 3
        }
    },
    methods: {
        select(btn, e) {
            e.preventDefault()
            if (btn == 1) {
                this.btn = 1
                this.activeColor = 'GREEN'
            }
            if (btn == 2) {
                this.btn = 2
                this.activeColor = 'RED'
            }
            if (btn == 3) {
                this.btn = 3
                this.activeColor = 'YELLOW'
            }
        }
    }
}
</script>

<style>

</style>