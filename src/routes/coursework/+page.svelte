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
