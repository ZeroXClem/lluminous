<script lang="ts">
	export let variant = 'secondary';
	let className = '';
	export { className as class };

	const variantClass = {
		small: 'border bg-white border-slate-300 hover:border-slate-400 transition-colors text-slate-600 text-sm px-3 py-1.5 rounded-md',
		outline:
			'border bg-white border-slate-300 hover:border-slate-400 transition-colors text-slate-600 text-sm px-3 py-1.5 rounded-lg',
		'outline-small':
			'border bg-white border-slate-300 hover:border-slate-400 transition-colors text-slate-600 text-xs px-3 py-1.5 rounded-lg',
	}[variant];
</script>

<button class="{className} {variantClass} flex items-center" on:click>
	<slot />
</button>
