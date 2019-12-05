<template>
	<div id="chart"></div>
</template>
<script>
	import * as G2Plot from '@antv/g2plot'

	const data = [{
			"x": "2019-03",
			"y": 385,
			"serie": "Paris"
		},
		{
			"x": "2019-04",
			"y": 888,
			"serie": "Paris"
		},
		{
			"x": "2019-05",
			"y": 349,
			"serie": "Paris"
		},
		{
			"x": "2019-06",
			"y": 468,
			"serie": "Paris"
		},
		{
			"x": "2019-07",
			"y": 477,
			"serie": "Paris"
		},
		{
			"x": "2019-03",
			"y": 291,
			"serie": "London"
		},
		{
			"x": "2019-04",
			"y": 484,
			"serie": "London"
		},
		{
			"x": "2019-05",
			"y": 293,
			"serie": "London"
		},
		{
			"x": "2019-06",
			"y": 147,
			"serie": "London"
		},
		{
			"x": "2019-07",
			"y": 618,
			"serie": "London"
		}
	];
	const config = {
		"title": {
			"visible": true,
			"text": "折线图"
		},
		"description": {
			"visible": true,
			"text": "一个简单的折线图"
		},
		"padding": "auto",
		"legend": {
			"visible": true,
			"position": "top-left",
			"wordSpacing": 4,
			"flipPage": false
		},
		"tooltip": {
			"visible": false,
			"shared": true,
			"crosshairs": {
				"type": "y"
			}
		},
		"xAxis": {
			"visible": true,
			"autoHideLabel": false,
			"autoRotateLabel": false,
			"autoRotateTitle": false,
			"grid": {
				"visible": false
			},
			"line": {
				"visible": false
			},
			"tickLine": {
				"visible": true
			},
			"label": {
				"visible": true
			},
			"title": {
				"visible": false,
				"offset": 12,
				"title": "日期"
			}
		},
		"yAxis": {
			"visible": true,
			"autoHideLabel": false,
			"autoRotateLabel": false,
			"autoRotateTitle": true,
			"grid": {
				"visible": true
			},
			"line": {
				"visible": false
			},
			"tickLine": {
				"visible": false
			},
			"label": {
				"visible": true
			},
			"title": {
				"visible": false,
				"offset": 12,
				"title": "数值"
			}
		},
		"label": {
			"visible": false,
			"type": "point"
		},
		"connectNulls": false,
		"smooth": false,
		"lineSize": 2,
		"lineStyle": {
			"lineJoin": "round",
			"lineCap": "round"
		},
		"point": {
			"visible": false,
			"size": 3,
			"shape": "circle",
			"style": {
				"stroke": "#fff"
			}
		},
		"forceFit": false,
		"animation": false,
		"width": 560,
		"height": 376,
		"xField": "x",
		"yField": "y",
		"seriesField": "serie",
		"color": null
	}

	export default {
		name: "Chart",

		data() {
			return {}
		},

		mounted() {
			const container = document.getElementById('chart');

			const plot = new G2Plot.Line(container, {
				data,
				...config,
			});
			plot.render();


		}
	}
</script>

<style>
</style>
