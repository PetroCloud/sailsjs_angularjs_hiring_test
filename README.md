

# 8-hours SailsJS+AngularJS hiring test  
  
``  
Run: npm install && sails lift  
``  
  
## Introduction

This exercise will help us determine your coding skills and habits. The mandatory part has to be totally fullfilled before we evaluate the bonus part. The bonus part doesn’t have to be entirely done if you don’t have the time to do it correctly. Please do this exercise on a normal 8 hours workday so we can evaluate your workload.
If you have any questions or concerns about that document or our expectations, please feel free to contact us. Asking the right questions is considered positively.

### Mandatory part
Implement a SailsJS/AngularJS webapp that accepts a JSON dataset (see dataset sample below) to render a D3JS traversable pie chart.
- The user should be able to input the dataset as copy/paste or upload 
- The dataset is saved in a sails-disk database adapter
- AngularJS application is served in assets/
- All graphical elements use AngularJS Material
- A bash script launches the app from a clean git clone

### Pie chart
The pie-chart will represent data in the following architecture, with the first data field in the center and going outwards :
1. regions
2. contract type
3. establishment type

When clicking a dataset, the chart adjusts to this sub-set. For instance, clicking one region will fill the inner circle with this region and let the place to this region’s contract types only, represented on the second ring. Selecting one contract type modifies the chart with our selected region on the first ring, our selected contract type on the second ring, and all establishment types for that region and that type of contract on the third ring.  

### Dataset format sample
```json
{  
    establishments: [  
	{  
		name: "cherdak",  
		type: "bar"  
		region: "minskaja"  
		contracts: [  
			{ type: "live", amount: 1500 }, 
			{ type: "radio", amount: 1400 } 
		]
	},  
	{  
		name: "revolucion",  
		type: "hotel",  
		region: "minskaja",  
		contracts: [  
			{ type: "radio", amount: 1800 } 
		]  
	}]
}
```
