<template>
    <div>
        <NuxtLink to="/" :style="{ fontSize: `${size}px`, margin: `${size / 4}px 0px` }">
            <p>yihe.ee</p>
        </NuxtLink>
    </div>
</template>

<style scoped>
div {
    display: flex;
    width: fit-content;
    height: fit-content;
    align-items: center;
    justify-content: center;
}

p {
    font-family: 'Courgette';
    user-select: none;
    cursor: pointer;
}

</style>

<script setup>
const props = defineProps({
    size: {
        type: String,
        default: "24"
    }
})
</script>