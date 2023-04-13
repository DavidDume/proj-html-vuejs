<template>
    <div class="show-templatete pointer">
        <h3>{{ title }}</h3>
    </div>
</template>

<script>

    export default {
        name: 'ShowTemplate',
        props: {
            title: String
        }
    }

</script>


<style lang="scss">
    @use '../styles/variables' as *;
    .show-templatete {
        background-color: $red;
        &:hover {
            background-color: white;
            
        }
        & h3 {
            text-transform: uppercase;
            color: white;
            text-align: center;
            font-weight: 300;
            padding: 25px;
            font-size: 12px;
            &:hover {
                color: black;
            }
        }
    }
</style>