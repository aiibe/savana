<script>
	import { modal } from '$lib/store'
</script>

<div class="modal is-active">
	<div class="modal-background" on:click="{() => modal.set(false)}"></div>
	<div class="modal-content">
		<div class="box content">
			<h1>Login</h1>
		</div>
	</div>
</div>