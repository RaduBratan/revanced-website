<script lang="ts">
let _title: string = "";
$: title = _title === "" ? "ReVanced" : `ReVanced · ${_title}`;

export { _title as title };

export let description: string = "Continuing the legacy of Vanced.";
</script>

<svelte:head>
  <title>{title}</title>
  <meta name="description" content={description} />
	<meta name="theme-color" content="#9FD5FF" />

  <!-- OpenGraph -->
	<meta property="og:title" content={title} />
	<meta property="og:description" content={description} />
	<meta property="og:type" content="website" />
	<meta property="og:image" content="/embed.png" />

  <!-- Twitter -->
	<meta name="twitter:title" content={title} />
	<meta name="twitter:description" content={description} />
	<meta name="twitter:image" itemprop="image" content="/embed.png" />
	<meta name="twitter:card" content="summary" />
</svelte:head>
