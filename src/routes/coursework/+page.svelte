<script lang="ts">
	let courses = [
		'Biomechanics',
		'Deep Learning in Computer Vision',
		'Mechanics and Control of Serial Manipulators',
		'Control of Automotive Systems',
		'Non-Linear Control',
		'Process Optimisation',
		'Optimal Control',
		'Non-Linear Dynamics',
		'Graph Theory',
		'Linear Algebra',
		'Signal Processing of Mechanical Systems',
		'Virtual Reality Engineering',
		'Computational Methods in Engineering',
		'Introduction to Data Analysis',
		'Measurements, Instrumentation and Control',
		'Variational Principles in Mechanics',
		'Finite Element Analysis'
	];

	let TA_stuff = [
		[
			'The Joy of Programming in Python',
			'https://www.youtube.com/playlist?list=PLmwjlGnmkZNvSAdN63aiGz9YML1Imdc65'
		],
		['Mechatronics', 'https://www.youtube.com/playlist?list=PLmwjlGnmkZNsg-e4GDFsaStVmi49QHKCg'],
		['Engineering Drawing'],
		['Finite Element Analysis']
	];
</script>

<div class="p-9 lg:p-20">
	<h3 class="text-5xl">Courses I have taken</h3>
	<ul>
		{#each TA_stuff as t}
			<li>
				<b>{t[0]}</b>
				{#if t.length > 1}<span>: <a href={t[1]}>Click here for the videos!</a> </span>
				{/if}
			</li>
		{/each}
	</ul>
	<h3 class="text-5xl">Courses I have done</h3>
	<ul>
		{#each courses as course}
			<li>{course}</li>
		{/each}
	</ul>
</div>
