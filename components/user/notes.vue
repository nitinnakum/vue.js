<template>
    <div class="flex flex-col items-center">
        <h1 class="text-2xl font-bold text-gray-700">Notes</h1>
        <textarea name="notes" id="notes" cols="40" rows="3" class="border border-solid border-black rounded my-3"></textarea>
            <button class="bg-sky-400 rounded text-sm font-medium p-2 ml-56 w-[79px] ">add notes</button>
    </div>
</template>
<script>
export default{
    name : "componentsUserNotes"
}
</script>