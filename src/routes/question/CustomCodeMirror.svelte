<script>
	import CodeMirror from 'svelte-codemirror-editor';
	/**
	 * @type {string}
	 */
	export let value;
	/**
	 * @type {any}
	 */
	export let theme;
	/**
	 * @type {any}
	 */
	export let lang;
</script>

<CodeMirror bind:value lang={lang()} {theme} />
