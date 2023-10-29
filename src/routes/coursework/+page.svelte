<script lang="ts">
	let courses = [
		'Control of Automotice Systems',
		'Non-Linear Control',
		'Measurements, Instrumentation and Control',
		'Process Optimisation',
		'Optimal Control',
		'Non-Linear Dynamics',
		'Graph Theory',
		'Linear Algebra',
		'Signal Processing of Mechanical Systems',
		'Mechanics and Control of Serial Manipulators',
		'Virtual Reality Engineering',
		'Deep Learning in Computer Vision',
		'Introduction to Data Analysis',
		'Finite Element Analysis',
		'Biomechanics',
		'Variational Principles in Mechanics',
		'Computational Methods in Engineering'
	];
</script>

<div class="p-9 lg:p-20">
	This page will also later contain the links to the courses I have taken
	<h3 class="text-5xl">Courses I have taken</h3>
	<ul>
		<li>The Joy of Programming in Python</li>
		<li>Mechatronics</li>
		<li>Engineering Drawing</li>
		<li>Finite Element Analysis</li>
	</ul>
	<h3 class="text-5xl">Courses I have done</h3>
	<ul>
		{#each courses as course}
			<li>{course}</li>
		{/each}
	</ul>
</div>
