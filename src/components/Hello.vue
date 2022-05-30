<template>
<h1> Learning Interpolation </h1>
<h2> {{ message }} </h2>
<h2> {{ number }} </h2>
<h2> {{ phone == "03411126905" }} </h2>
<h1> {{ name("Siddique") }} </h1>

<p> {{ myProfile() }} </p>
<p> {{ myProfile().phone }} </p>

<button v-on:click="getData()"> Click me </button>
<button v-on:dblclick="getData()"> Click me double </button>
<button v-on:mouseover="getData()"> Mouse over on me </button>

<br />
<button v-on:click="subtract()"> -- </button>
<h1> {{ counter }} </h1>
<button v-on:click="add()"> ++ </button>
</template>

<script>
export default {
    name: "AbHello",
    data() {
        return {
            message: "This is my message.",
            number: 23,
            phone: "03411126905",
            counter: 0,
            name: function (cast) {
                return "Arsalan Ahmed " + cast
            }
        }
    },
    methods: {
        myProfile() {
            return {
                "name": "Arsalan Ahmed Siddique",
                "email": "email@test.com",
                "phone": this.phone
            }
        },
        getData() {
            // alert("Clicked successfully.")
            console.warn('Mouse over successfully. ')
        },
        add() {
            this.counter = this.counter + 1;
        },
        subtract() {
            this.counter = this.counter - 1;
        }
    }
}
</script>

<style scoped>
h1 {
    color: red;
}
</style>
