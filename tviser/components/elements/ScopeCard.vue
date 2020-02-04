<template>
    <a :href="localePath(`/scope/${id}`)" class="scope-card" @click.prevent="$bus.goTo(`/scope/${id}`,$router,localePath)">
        <div class="scope-card-header">
            <svg-icon name="work" style="width: 70px;height: 60px"/>
        </div>
        <div class="scope-card-body">
            <span>Web-design</span>
        </div>
    </a>
</template>

<script>
    export default {
        props: {
            id: Number,
        },
    }
</script>

<style scoped>

</style>
