<script lang="ts">
    // import PhoneNumberInput from "$lib/components/PhoneNumberInput.svelte";
    // import TextInput from "$lib/components/TextInput.svelte";
    export let title: string = "";
    export let forumData: any[];
</script>

<div class="bg-transparent">
    {#if title}
        <h1 class="text-5xl font-bold text-green">{title}</h1>
    {/if}

    {#each forumData as section (section.title)}
        <div>
            <h1>{section.title}</h1>

            <!-- {#each section.fields as field} -->
            <!--     {#if field.type === "phone"} -->
            <!--         <PhoneNumberInput {...field.data} /> -->
            <!--     {:else} -->
            <!--         <TextInput {...field.data} /> -->
            <!--     {/if} -->
            <!-- {/each} -->
        </div>
    {/each}
</div>
