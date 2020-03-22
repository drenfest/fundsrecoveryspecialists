<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<style>
	.content-section{
		display:flex;
		flex-direction:column;
		justify-content:center;
		align-items:center;
		align-content:center;
		max-width:1060px;
		margin: 6rem auto;
	}
	header{
		background-color:#031330;
		width:100%;
		border-radius:10px;
	}
	header h2{
		color:white;
		padding:1rem;
		margin:0;
		font-weight:bold;
	}
	.flex{
		display:flex;
		width:100%;
		justify-content:space-between;
	}
	main{
		padding:3rem;
		border-radius:10px;
		background: #64b0d6; /* Old browsers */
		background: -moz-linear-gradient(top, #64b0d6 0%, #ffffff 79%); /* FF3.6-15 */
		background: -webkit-linear-gradient(top, #64b0d6 0%,#ffffff 79%); /* Chrome10-25,Safari5.1-6 */
		background: linear-gradient(to bottom, #64b0d6 0%,#ffffff 79%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
		filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#64b0d6', endColorstr='#ffffff',GradientType=0 ); /* IE6-9 */
		margin-top: -10px;
	}
	footer{
		position:relative;
	}
	.cover-top{
		display:none;
	}
	.footer-nav{
		display:flex;
		justify-content:center;
	}
	hr{
		background: lightgrey;
		color: #f2f2f2;
		border: 1px solid #efefef;
		margin-top: 1rem;
	}
	@media screen and (min-width:768px){
		.cover-top{
			display:block;
			margin-top: -105px;
			max-height: 200px;
		}
	}
</style>
<div class="content-section">
	<header>
		<h2>Funds Recovery Specialist</h2>
	</header>
	<div class="flex">
		<Nav {segment}/>
		<img class="fr cover-top" src="/assets/images/money-top.png" alt="Money Popping Out Of The Top Of The Nav"/>
		<div class="clear"></div>
	</div>


	<main>
		<slot></slot>
		<footer>
			<img class="fl" src="/assets/images/cash-stack.png" alt="Money Saved From Our Services"/>
			<p>These funds are held for only a brief period of time, after that time elapses the agency responsible for them may be permitted to seize them permanently through a process called "escheatment."</p>
			<p>We believe it's wrong for private citizens to lose their funds to faceless government agencies (a system rooted in feudal 16th century England). We are determined to prevent this from happening to any person, including you.</p>
		<div class="clear"> </div>
		</footer>
		<hr>
		<div class="footer-nav">
			<Nav {segment}></Nav>
		</div>
	</main>
</div>

