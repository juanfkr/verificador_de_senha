<template>
        <p>{{ warning }}</p>
    <section>
        <div :style="strengthByLength" class="hr"></div>
    </section>
</template>

<script setup>
import { computed } from 'vue';
import { ref } from 'vue'

const props = defineProps({
    passwordStrength: {
        type: String,
        required: true
    }
})

const warning = ref();

const strengthByLength = computed(() => {
    if(props.passwordStrength.length >= 1 && props.passwordStrength.length <= 4) {
        warning.value = 'Senha fraca'
        return 'width: 25%; background: white;';
    } else if (props.passwordStrength.length >= 5 && props.passwordStrength.length <= 10) {
        warning.value = 'Senha média'
        return 'width: 50%; background: red;';
    } else if (props.passwordStrength.length >= 11 && props.passwordStrength.length <= 14) {
        warning.value = 'Senha forte'
        return 'width: 75%; background: orange;';
    } else if (props.passwordStrength.length >= 15) {
        warning.value = 'Senha muito forte'
        return 'width: 100%; background: lime;';
    } else {
        warning.value = 'Insira sua senha';
        return 'width: 0%; background: none;'
    }
})


</script>

<style scoped>
    section {
        width: 100%;
        border: 2px solid rgba(0, 0, 0, 0.274);
        border-radius: 8px;

        .hr {
            width: 0%;
            height: .5em;
            border-radius: inherit;
            transition: all .3s ease-in-out;
        }
    }


</style>