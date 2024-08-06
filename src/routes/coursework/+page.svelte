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
		['Physics for Class XI (offline in Bala Vidya Mandir!)'],
		['Human Movement Science (NPTEL)'],
		// ['Human Movement Science (NPTEL)', 'https://nptel.ac.in/courses/109106401'],
		['Manufacturing Processes (ME2300: Jan-May 2024)'],
		['The Joy of Programming in Python (NPTEL)'],
		// [
		// 	'The Joy of Programming in Python (NPTEL)',
		// 	'https://www.youtube.com/playlist?list=PLmwjlGnmkZNvSAdN63aiGz9YML1Imdc65'
		// ],
		['Mechatronics (NPTEL)'],
		// ['Mechatronics', 'https://www.youtube.com/playlist?list=PLmwjlGnmkZNsg-e4GDFsaStVmi49QHKCg'],
		['Engineering Drawing'],
		['Finite Element Analysis']
	];
</script>

<div class="m-1 p-9 lg:px-20 lg:py-10">
	<h3 class="text-5xl">Courses I have taught</h3>
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
