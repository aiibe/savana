<script>
	import { modal } from '$lib/store'

	// Form inputs
	let email = ''
	let password = ''

	function handleSubmit() {

	}

	function abort() {
		email = ''
		password = ''
		modal.set(false)
	}
</script>

<div class="modal is-active">
	<div class="modal-background" on:click="{() => modal.set(false)}"></div>
	<div class="modal-content">
		<div class="box content">
			<h3>Create your account</h3>
			<p>Publish and share your content</p>
			<form on:submit|preventDefault={handleSubmit}>
				<div class="field">
					<label class="label">Email</label>
					<div class="control">
						<input class="input" type="email" bind:value={email}>
					</div>
				</div>
				<div class="field">
					<label class="label">Password</label>
					<div class="control">
						<input class="input" type="password" bind:value={password}>
					</div>
				</div>
				<div class="field is-grouped is-grouped-right">
					<p class="control">
						<a class="button is-success">Submit</a>
					</p>
					<p class="control">
						<a class="button is-light" on:click={abort}>Cancel</a>
					</p>
				</div>
			</form>
		</div>
	</div>
</div>