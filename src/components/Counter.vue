<template>
    <div class="container">
        <div class="row">
            <div class="col-md-4">
                <div class="card shadow-lg">
                    <div class="card-body">
                        <p class="h3 display">{{this.count}}</p>
                        <button @click="incr" class="btn btn-success m-1">Increment</button>
                        <button @click="decr" class="btn btn-warning m-1">Decrement</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Counter",
    data: function(){
        return {
            count: 0
        };
    },
    methods: {
        incr: function(){
            this.count = this.count + 1;
        },
        decr: function(){
            this.count = this.count - 1;
        }
    }
};
</script>

<style scoped>

</style>