<script lang="ts">
</script>

{#if $$props.href}
	<svelte:element
		this="a"
		href={$$props.href}
		{...$$restProps}
		class={$$props.class}
		on:click
		on:change
		on:keydown
		on:keyup
		on:touchstart
		on:touchend
		on:touchcancel
		on:mouseenter
		on:mouseleave
	>
		<slot />
	</svelte:element>
{:else}
	<svelte:element
		this="button"
		{...$$restProps}
		class={$$props.class}
		on:click
		on:change
		on:keydown
		on:keyup
		on:touchstart
		on:touchend
		on:touchcancel
		on:mouseenter
		on:mouseleave
	>
		<slot />
	</svelte:element>
{/if}

<style>
	.test {
		color: red;
	}
	button {
		background: #000;
		color: #fff;
		border-radius: 9999px;
		padding: 10px 20px;
	}
</style>
