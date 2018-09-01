downsample-lttb
===============

Largest Triangle Three Buckets downsample algorithm by Sveinn Steinarsson reshaped into a node.js module.

This is useful for downsampling large dataseries in order to be able to plot a representative chart shape with a manageable amount of data points.
	
# Instructions

Install with

	npm install git+https://github.com/pingec/downsample-lttb.git

Usage example

	var downsampler = require("downsample-lttb");
	
	//provide a series as an array of [x,y] pairs
	var dummyDataSeries = [[1,2],[2,2],[3,3],[4,3],[5,6],[6,3],[7,3],[8,5],[9,4],[10,4],[11,1],[12,2]];

	//pass the series and number of desired datapoints
	var downsampledSeries = downsampler.processData(dummyDataSeries, 3);
	
	console.log(downsampledSeries);	
	//outputs [ [ 1, 2 ], [ 5, 6 ], [ 12, 2 ] ]

# Downsampled chart series examples
###\# of samples: 8614  downsampled to: 500
![500 datapoints](https://raw.githubusercontent.com/pingec/downsample-lttb/master/screenshots/500.png)
### \# of samples: 8614  downsampled to: 200
![200 datapoints](https://raw.githubusercontent.com/pingec/downsample-lttb/master/screenshots/200.png)
### \# of samples: 8614  downsampled to: 100
![100 datapoints](https://raw.githubusercontent.com/pingec/downsample-lttb/master/screenshots/100.png)
### \# of samples: 8614  downsampled to: 50
![50 datapoints](https://raw.githubusercontent.com/pingec/downsample-lttb/master/screenshots/50.png)
