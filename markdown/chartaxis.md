# ChartAxis Object (JavaScript API for Excel)

Represents a single axis in a chart.

## Properties

| Property	   | Type	|Description| Req. Set|
|:---------------|:--------|:----------|:----|
|axisGroup|string|Represents the group for the specified axis. Read-only. Possible values are: Primary, Secondary.|[1.8](../requirement-sets/excel-api-requirement-sets.md)|
|baseTimeUnit|string|Returns or sets the base unit for the specified category axis. Possible values are: Days, Months, Years.|[1.8](../requirement-sets/excel-api-requirement-sets.md)|
|categoryType|string|Returns or sets the category axis type. Possible values are: Automatic, TextAxis, DateAxis.|[1.8](../requirement-sets/excel-api-requirement-sets.md)|
|customDisplayUnit|double|Represents the custom axis display unit value. Read Only. To set this property, please use the SetCustomDisplayUnit(double) method. Read-only.|[1.8](../requirement-sets/excel-api-requirement-sets.md)|
|displayUnit|string|Represents the axis display unit. Possible values are: None, Hundreds, Thousands, TenThousands, HundredThousands, Millions, TenMillions, HundredMillons, Billions, Trillions, Custom.|[1.8](../requirement-sets/excel-api-requirement-sets.md)|
|logBase|double|Represents the base of the logarithm when using logarithmic scales.|[1.8](../requirement-sets/excel-api-requirement-sets.md)|
|majorTimeUnitScale|string|Returns or sets the major unit scale value for the category axis when the CategoryType property is set to TimeScale. Possible values are: Days, Months, Years.|[1.8](../requirement-sets/excel-api-requirement-sets.md)|
|majorUnit|object|Represents the interval between two major tick marks. Can be set to a numeric value or an empty string.  The returned value is always a number.|[1.1](../requirement-sets/excel-api-requirement-sets.md)|
|maximum|object|Represents the maximum value on the value axis.  Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.|[1.1](../requirement-sets/excel-api-requirement-sets.md)|
|minimum|object|Represents the minimum value on the value axis. Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.|[1.1](../requirement-sets/excel-api-requirement-sets.md)|
|minorTimeUnitScale|string|Returns or sets the minor unit scale value for the category axis when the CategoryType property is set to TimeScale. Possible values are: Days, Months, Years.|[1.8](../requirement-sets/excel-api-requirement-sets.md)|
|minorUnit|object|Represents the interval between two minor tick marks. "Can be set to a numeric value or an empty string (for automatic axis values). The returned value is always a number.|[1.1](../requirement-sets/excel-api-requirement-sets.md)|
|scaleType|string|Represents the value axis scale type. Possible values are: Linear, Logarithmic.|[1.8](../requirement-sets/excel-api-requirement-sets.md)|
|showDisplayUnitLabel|bool|Represents whether the axis display unit label is visible.|[1.8](../requirement-sets/excel-api-requirement-sets.md)|
|type|string|Represents the axis type. Read-only. Possible values are: Invalid, Category, Value, SeriesAxis.|[1.8](../requirement-sets/excel-api-requirement-sets.md)|

_See property access [examples.](#property-access-examples)_

## Relationships
| Relationship | Type	|Description| Req. Set|
|:---------------|:--------|:----------|:----|
|format|[ChartAxisFormat](chartaxisformat.md)|Represents the formatting of a chart object, which includes line and font formatting. Read-only.|[1.1](../requirement-sets/excel-api-requirement-sets.md)|
|majorGridlines|[ChartGridlines](chartgridlines.md)|Returns a gridlines object that represents the major gridlines for the specified axis. Read-only.|[1.1](../requirement-sets/excel-api-requirement-sets.md)|
|minorGridlines|[ChartGridlines](chartgridlines.md)|Returns a Gridlines object that represents the minor gridlines for the specified axis. Read-only.|[1.1](../requirement-sets/excel-api-requirement-sets.md)|
|title|[ChartAxisTitle](chartaxistitle.md)|Represents the axis title. Read-only.|[1.1](../requirement-sets/excel-api-requirement-sets.md)|

## Methods

| Method		   | Return Type	|Description| Req. Set|
|:---------------|:--------|:----------|:----|
|[setCategoryNames(sourceData: Range)](#setcategorynamessourcedata-range)|void|Sets all the category names for the specified axis.|[1.8](../requirement-sets/excel-api-requirement-sets.md)|
|[setCustomDisplayUnit(value: double)](#setcustomdisplayunitvalue-double)|void|Sets the axis display unit to a custom value.|[1.8](../requirement-sets/excel-api-requirement-sets.md)|

## Method Details


### setCategoryNames(sourceData: Range)
Sets all the category names for the specified axis.

#### Syntax
```js
chartAxisObject.setCategoryNames(sourceData);
```

#### Parameters
| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|sourceData|Range|The Range object corresponding to the source data.|

#### Returns
void

### setCustomDisplayUnit(value: double)
Sets the axis display unit to a custom value.

#### Syntax
```js
chartAxisObject.setCustomDisplayUnit(value);
```

#### Parameters
| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|value|double|value.|

#### Returns
void
### Property access examples
Get the `maximum` of Chart Axis from Chart1

```js
Excel.run(function (ctx) { 
	var chart = ctx.workbook.worksheets.getItem("Sheet1").charts.getItem("Chart1");	
	var axis = chart.axes.valueAxis;
	axis.load('maximum');
	return ctx.sync().then(function() {
			console.log(axis.maximum);
	});
}).catch(function(error) {
		console.log("Error: " + error);
		if (error instanceof OfficeExtension.Error) {
			console.log("Debug info: " + JSON.stringify(error.debugInfo));
		}
});
```

Set the  `maximum`,  `minimum`,  `majorunit`, `minorunit` of valueaxis. 

```js
Excel.run(function (ctx) { 
	var chart = ctx.workbook.worksheets.getItem("Sheet1").charts.getItem("Chart1");	
	chart.axes.valueAxis.maximum = 5;
	chart.axes.valueAxis.minimum = 0;
	chart.axes.valueAxis.majorUnit = 1;
	chart.axes.valueAxis.minorUnit = 0.2;
	return ctx.sync().then(function() {
			console.log("Axis Settings Changed");
	});
}).catch(function(error) {
		console.log("Error: " + error);
		if (error instanceof OfficeExtension.Error) {
			console.log("Debug info: " + JSON.stringify(error.debugInfo));
		}
});
```
