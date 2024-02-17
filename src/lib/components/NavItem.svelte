<script lang="ts">
    export let name: string;
    export let href: string;
    export let style: string = "";
</script>

{#if style}
    <a
        {href}
        class="bg-green/80 hover:bg-green/100 transition-all text-xl text-base rounded-md p-2 font-bold"
        >{name}</a
    >
{:else}
    <a {href} class="hover:text-green transition-all text-xl">{name}</a>
{/if}
