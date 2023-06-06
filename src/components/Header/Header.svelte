<script lang="ts">
    export let content: string
</script>


<h1 on:input={()=>{ console.log("Just changed") }} contenteditable="true" class="break-words font-bold text-2xl">{content}</h1>
