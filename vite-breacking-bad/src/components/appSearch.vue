<script>
export default {
    name: "appSearch",
};
</script>

<template>
    <select name="series" id="" onchange="$emit(`changed`)">
        <option value="">Select category</option>
        <option value="breakingBad">Breaking Bad</option>
        <option value="betterCallSoul">Better Call Soul</option>
    </select>
</template>

<style>
</style>
