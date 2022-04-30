<script>
	import '@toast-ui/chart/dist/toastui-chart.css';
	import { onMount } from 'svelte';

	export let data = {
		categories: ['one', 'two'],
		series: [
			{
				name: 'amaount',
				data: [1, 2]
			}
		]
	};

	let chart;

	const options = {
		chart: { title: 'Average Temperature', width: 900, height: 400 },
		xAxis: { pointOnColumn: false, title: { text: 'Month' } },
		yAxis: { title: 'Temperature (Celsius)' }
	};

	onMount(async () => {
		const el = document.getElementById('chart-area');
		const ChartImport = await import('@toast-ui/chart');
		const Chart = ChartImport.default;
		chart = Chart.areaChart({
			el,
			data,
			options
		});
	});
</script>

<div id="chart-area" />
