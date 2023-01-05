<script lang="ts">
	import toast, { Toaster } from 'svelte-french-toast';
	const opts = { id: 'my-toast' };
	const showToast = () => {
		toast.loading('please wait...', opts);
		setTimeout(() => {
			toast.success('Success', opts);
		}, 2000);
	};
</script>

<h1>Toast Demo</h1>
<button on:click={showToast}> Show toast </button>

<Toaster />
