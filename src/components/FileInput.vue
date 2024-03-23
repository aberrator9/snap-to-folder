<script setup>
    import { ref } from 'vue'

    const currentFolder = ref('')
</script>

<template>
    <select name="folder" id="folder-select">
        <option value="">{{ currentFolder != '' ? currentFolder : 'Choose folder' }}</option>
        <option value="new">New folder</option>
    </select>
    <div>
        <input
        type="file"
        @change="onFileChanged($event)"
        accept="image/*"
        capture
        />
    </div>
</template>