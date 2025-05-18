<template>
    <div class="flex flex-col items-center justify-center h-screen">
        <div class="w-full text-center mb-6">
            <slot name="header"></slot>
        </div>
        <slot name="body"></slot>
    </div>
</template>