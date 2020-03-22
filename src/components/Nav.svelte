<script>
	export let segment;
</script>

<style>
	nav {
		font-weight: 300;
		padding: 0 1em;
	}

	ul {
		margin: 0;
		padding: 0;
		list-style:none;
	}




	[aria-current] {
		position: relative;
		display: inline-block;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
		color:#235eb5;
		font-weight:bold;
	}
	@media screen and (min-width: 768px){
		li {
			display: block;
			float: left;
		}
	}
</style>

<nav>
	<ul>
		<li><a aria-current='{segment === undefined ? "page" : undefined}' href='.'>Home</a></li>
		<li><a aria-current='{segment === "our-company" ? "page" : undefined}' href='our-company'>Our Company</a></li>
		<li><a aria-current='{segment === "how-it-works" ? "page" : undefined}' href='how-it-works'>How It Works</a></li>
		<li><a aria-current='{segment === "questions" ? "page" : undefined}' href='questions'>Questions</a></li>
		<li><a aria-current='{segment === "contact" ? "page" : undefined}' href='contact'>Contact</a></li>
	</ul>
</nav>
