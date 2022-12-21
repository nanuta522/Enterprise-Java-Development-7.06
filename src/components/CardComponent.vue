<template>
    <div class="col-auto">
        <div class="card g-5 element" style="width: 18rem;">
            <h3>{{ card.title }}</h3>

            <div class="card-body">
                <h5><em>{{ card.description }}</em></h5>

                <p class="card-text">{{ card.content }}</p>
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
    props: {
        card: {
            type: Object
        }
    }
}
</script>

<style>
.element {
    padding: 1rem 0;
    text-align: center;
}

.card-body {
    height: 7rem;
}
</style>