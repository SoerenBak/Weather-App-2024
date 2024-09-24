<script setup>
defineProps({
    day: Object
})
</script>

<template>
    <div class="mb-2 flex items-center justify-between">
        <table class="w-full">
            <tr>
                {{ new Date(day.date).toLocaleDateString('da-dk', { weekday: 'long' }) }}

                <td class="w-1/3">
                    <img :src="day.day.condition.icon" alt="icon" width="30" class="mx-auto" />
                </td>

                {{ Math.round(day.day.maxtemp_c) }} / {{ Math.round(day.day.mintemp_c) }}
            </tr>
        </table>
    </div>
</template>