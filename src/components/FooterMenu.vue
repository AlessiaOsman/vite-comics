<script>
export default {
    name: 'FooterMenu',
    props: {
        title: String,
        links: Array,
    }
}
</script>
<template>
    <h2>{{ title }}</h2>
    <ul>
        <li v-for="link in links" :key="link.id">
            <a :href="link.url">
                {{ link.text }}
            </a>
        </li>
    </ul>
</template>
<style lang="scss" scoped>
h2 {
        color: #ffffff;
        margin: 16px 0;
    }

    ul {
        list-style-type: none;
        display: flex;
        flex-direction: column;
        gap: 8px;

        li a {
            color: #ffffff;
        }

    }
</style>