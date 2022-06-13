<template>
    <div>
        <div class="flex w-full max-h-32 text-white border-b p-4">
            <div class="flex flex-col w-full hidden md:flex items-end justify-center pr-4">
                <h2 class="text-2xl">{{ titulo }}</h2>
                <a class="text-xl"><strong></strong>{{ entrega }}</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MyHeader',
    props: {
        titulo: {
            type: String,
            required: true,
        },
        entrega: {
            type: String,
            required: true,
        }
    }
}
</script>