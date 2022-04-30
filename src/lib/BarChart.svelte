<script>
	import '@toast-ui/chart/dist/toastui-chart.css';
	import { onMount } from 'svelte';

	export let data = {
		categories: ['one', 'two'],
		series: [
			{
				name: 'amount',
				data: [1, 2]
			}
		]
	};

	let chart;

	const options = {
		chart: { width: 700, height: 400 }
	};

	onMount(async () => {
		const el = document.getElementById('chart-area');
		const ChartImport = await import('@toast-ui/chart');
		const Chart = ChartImport.default;
		chart = Chart.barChart({
			el,
			data,
			options
		});
	});
</script>

<div id="chart-area" />
