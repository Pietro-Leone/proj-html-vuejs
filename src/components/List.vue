<script>
export default {
    props: {
        navElements: {
            type: Array,
            required: true,
        }
    },
}
</script>

<template>
    <ul class="navbar-nav d-flex flex-row">
        <li class="nav-item text-center" v-for="element in navElements">
            <a class="nav-link" href="#">{{ element }}</a>
        </li>
    </ul>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

a {
    &::after {
        content: " ";
        position: absolute;
        left: 8px;
        top: 0px;
        width: calc(100% - 16px);
        height: 2px;
        background: $color-primary;
        z-index: 30;
        transition: .5s transform;
        opacity: 0;
    }

    &:hover {
        &::after {
            transform: translateY(40px);
            opacity: 1;
        }
    }
}

.nav-link {
    position: relative;
    text-transform: uppercase;
    color: $color-primary;
    font-weight: 500;
    padding: 8px !important;

    &:hover {
        color: $color-primary;
    }
}
</style>
