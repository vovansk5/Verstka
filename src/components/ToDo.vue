<template>
    <ul>
        <li v-for="item in todos" :key="item">
            {{item}}
            
        </li>
    </ul>
</template>

<script>
export default {
    name:'MyToDO'
}
</script>