<template lang="pug">
iframe(
    :class="$style.root"
    src="https://dev.technikastroy.ru/client"
)
</template>

<script lang="ts">
import { defineComponent, onMounted } from "vue"; 

export default defineComponent({
    name: 'Home',
    setup() {
        function onClick() {
            console.log('CLICK')
        }

        onMounted(() => {
            window.addEventListener('message', e => {
                console.log('event: ',e, )
            })
        })

        return {
            onClick
        }
    }
})
</script>

<style lang="scss" module>
.root {
    width: 100vw;
    height: 100vh;
}
</style>