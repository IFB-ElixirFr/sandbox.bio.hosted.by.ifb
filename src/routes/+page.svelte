<script>
import { Button, Icon } from "sveltestrap";
import { categories, explore, playgrounds } from "$stores/tutorials";
import Listings from "$components/Listings.svelte";
import TutorialList from "$src/components/TutorialList.svelte";
</script>

<svelte:head>
	<title>sandbox.bio</title>
</svelte:head>

<div class="container-fluid">
	<div class="row pb-0 pe-lg-0 bg-light align-items-center rounded-3 border shadow-lg">
		<div class="col-lg-6 p-3 p-lg-4 pt-lg-3">
			<h1 class="fw-bold text-center" style="font-size: 30px">Interactive bioinformatics tutorials</h1>
			<p class="lead my-4 text-center">
				Sandbox.bio is a free platform for bioinformatics command-line tutorials created by <a href="https://tinysite.dev/@robert"
					>Robert Aboukhalil</a
				>. It was set up by compiling bioinformatics command-line tools in WebAssembly (abbreviated Wasm) so that they could be run in the browser.
				<a href="https://www.france-bioinformatique.fr/en/home/">The French Bioinformatics Institute</a>
				hosts an instance of this platform at the initiative of its
				<a href="https://www.france-bioinformatique.fr/en/e-learning/">e-learning working group</a>, with the aim of meeting the needs of the French
				community. All the educational content has been created and made available by this working group. All feedback is welcome.
			</p>
			<div class="text-center">
				<Button size="lg" color="primary" href="/tutorials">Get started <Icon name="arrow-right" /></Button>
				<Button size="lg" color="outline-primary" href="/about">Learn more</Button>
				<Button size="lg" color="outline-primary" href="https://ifb-elixirfr.github.io/sandboxbio-IFB-docs/" target="_blank">Documentation</Button>
			</div>
		</div>
		<div class="align-center text-center col-lg-6 p-0 pb-2 overflow-hidden d-none d-md-inline">
			<img class="rounded-lg-3" src="/logoSandboxIFB.png" alt="Screenshot of terminal and exercises" width="500" />
		</div>
	</div>
</div>

<h3 class="mt-5">Tutorials</h3>
<TutorialList categories={$categories} />
<hr class="mt-5" />

<h3 class="mt-5">Playgrounds</h3>
<Listings items={$playgrounds} />

<!-- <hr class="mt-5" /> -->
<!-- <h3 class="mt-5">Explore</h3>
<Listings items={$explore} /> -->

<style>
.bg-light {
	background-color: rgb(232, 240, 240) !important;
}
</style>
