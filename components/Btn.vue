<template>
    <div>
        <NuxtLink :to="url" >
            <span>{{text}}</span>
        </NuxtLink>
    </div>

</template>

<script>
export default {
    props: {
        text: {
            type: String/* , 
            required: true */
        },
        url: {
            type: String
        }
    }
}
</script>