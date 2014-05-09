downsample-lttb
===============

Largest Triangle Three Buckets downsample algorithm by Sveinn Steinarsson reshaped into a node.js module.

This is useful for downsampling large dataseries in order to be able to plot a representative chart with a manageable amount of data points.
	
#Code example

	var downsampler = require("downsample-lttb");
	
	var dummyDataSeries = [[1,2],[2,2],[3,3],[4,3],[5,6],[6,3],[7,3],[8,5],[9,4],[10,4],[11,1],[12,2]];
	var downsampledSeries = downsampler.processData(dummyDataSeries, 3);
	
	console.log(downsampledSeries);	
	//outputs [ [ 1, 2 ], [ 5, 6 ], [ 12, 2 ] ]

#Downsampled chart series examples
###\# of samples: 8614  downsampled to: 500
![500 datapoints](screenshots/500.PNG)
###\# of samples: 8614  downsampled to: 200
![200 datapoints](screenshots/200.PNG)
###\# of samples: 8614  downsampled to: 100
![100 datapoints](screenshots/100.PNG)
###\# of samples: 8614  downsampled to: 50
![50 datapoints](screenshots/50.PNG)