<script>
	import { modal } from '$lib/store'
	import Signup from '$lib/Signup.svelte'
	import Login from '$lib/Login.svelte'
</script>

<nav class="navbar has-shadow">
	<div class="container">
		<div class="navbar-brand">
			<a href="/" class="navbar-item">
				<img src="/static/savana.png" alt="savana logo">
			</a>
		</div>
		<div class="navbar-menu">
			<div class="navbar-end">
				<div class="navbar-item">
					<button class="button" on:click="{() => modal.set('login') }">Login</button>
				</div>
				<div class="navbar-item">
					<button class="button is-success" on:click="{() => modal.set('signup') }">Signup</button>
				</div>
			</div>
		</div>
	</div>
</nav>

{#if $modal === 'signup'}
<Signup />
{:else if $modal === 'login'}
<Login />
{/if}