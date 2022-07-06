<template>
    <div class="page">
        <slot></slot>
    </div>
</template>

<script>
export default {
    name: "GlobalPageComponents",
}
</script>

<style lang="scss" scoped>
.page {
    padding-top: 6rem;
    background-color: #FFC71A;
}
</style>