<template>
    <h1>Employee Of The Month</h1>
    <h3>{{personData.name.first}} {{personData.name.last}} </h3>
    <p></p>
</template>

<script>
export default {
    name: 'EmployeeOfTheMonthPage',
    data() {
        return {
            personData: null,
        }
    },
    created() {
        fetch('https://randomuser.me/api/')
            .then(response => response.json())
            .then(data => this.personData = data.results[0])
    },
}
</script>

