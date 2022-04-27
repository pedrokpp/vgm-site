<script>

	import Section1 from "../components/sections/Section1.svelte";
	import Section2 from "../components/sections/Section2.svelte";
	import Section3 from "../components/sections/Section3.svelte";

	import AltDivider from "../components/dividers/AltDivider.svelte";
	
	import Footer from "../components/sections/Footer.svelte";

	import Video from "../components/sections/Video.svelte";

</script>

<div class="content">
	<Video />
	<Section1 />
	<Section2 />
	<AltDivider />
	<Section3 />
	<Footer />
</div>

<style>

	@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;300;500;700&display=swap');


	.content {
		--main-blue: #0c243c;
		--soft-blue: #053966;
		background-color: #0c243c;
		overflow: auto;
		width: 100%;
		height: 100%;
		font-family: 'Montserrat', sans-serif;
	}

</style>