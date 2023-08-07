<script setup  lang="ts">
import type { EventItem } from '@/type'
import type { PropType } from 'vue';
import { useRouter } from 'vue-router'

// defineProps({
//     event: {
//         type: Object as PropType<EventItem>,
//             require:true
//     }
// })
const props = defineProps ({
    event: {
        type: Object as PropType<EventItem>,
        require: true
    }
})
const router = useRouter()

function register() {
    router.push({
        name: 'event-detail',
        params: {
            id: props.event?.id
        }
    })
} 

</script>
<template>
       <p>Registration from here</p>
       <button @clik="register"> Register Me </button>
</template>
