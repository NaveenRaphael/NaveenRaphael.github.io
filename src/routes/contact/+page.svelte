<script lang="ts">
	const contact_details = new Map([
		['Email', 'ME22D009@smail.iitm.ac.in'],
		['Phone number', '8610751071']
	]);
</script>

<div class="p-9 lg:p-20">
	You can contact me at
	<ul>
		{#each contact_details as [c, v]}
			<li><b>{c}:</b> {v}</li>
		{/each}
	</ul>
</div>
