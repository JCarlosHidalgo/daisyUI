<script setup>
    defineProps({
        headerMessage: String,
        additionalDropdownStyle: String,
        additionalHeaderStyle: String
    })
</script>

<template>
    <div :class="'dropdown ' + additionalDropdownStyle">
        <div tabindex="0" role="button" :class="'btn '  + additionalHeaderStyle">
            {{ headerMessage }}
            <slot name="HeaderIcon"></slot>
        </div>
        <ul tabindex="-1" class="dropdown-content menu bg-base-100 rounded-box z-1 w-55 max-sm:w-46 p-2 shadow-sm mt-1">
            <slot name="Items"></slot>
        </ul>
    </div>
</template>