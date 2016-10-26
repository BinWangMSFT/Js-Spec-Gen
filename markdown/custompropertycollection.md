# CustomPropertyCollection Object (JavaScript API for Word)

_Word 2016, Word for iPad, Word for Mac, Word Online_

Contains the collection of [customProperty](customProperty.md) objects.

## Properties

| Property	   | Type	|Description| Req. Set|
|:---------------|:--------|:----------|:----|
|items|[CustomProperty[]](customproperty.md)|A collection of customProperty objects. Read-only.|[1.3](../reqset/word-requirement.md)|

_See property access [examples.](#property-access-examples)_

## Relationships
None


## Methods

| Method		   | Return Type	|Description| Req. Set|
|:---------------|:--------|:----------|:----|
|[deleteAll()](#deleteall)|void|Deletes all custom properties in this collection.|[1.3](../reqset/word-requirement.md)|
|[getCount()](#getcount)|int|Gets the count of custom properties.|[1.3](../reqset/word-requirement.md)|
|[getItem(key: string)](#getitemkey-string)|[CustomProperty](customproperty.md)|Gets a custom property object by its key, which is case-insensitive.|[1.3](../reqset/word-requirement.md)|
|[load(param: object)](#loadparam-object)|void|Fills the proxy object created in JavaScript layer with property and object values specified in the parameter.|[1.1](../reqset/word-requirement.md)|
|[set(key: string, value: object)](#setkey-string-value-object)|[CustomProperty](customproperty.md)|Creates or sets a custom property.|[1.3](../reqset/word-requirement.md)|

## Method Details


### deleteAll()
Deletes all custom properties in this collection.

#### Syntax
```js
customPropertyCollectionObject.deleteAll();
```

#### Parameters
None

#### Returns
void

### getCount()
Gets the count of custom properties.

#### Syntax
```js
customPropertyCollectionObject.getCount();
```

#### Parameters
None

#### Returns
int

### getItem(key: string)
Gets a custom property object by its key, which is case-insensitive.

#### Syntax
```js
customPropertyCollectionObject.getItem(key);
```

#### Parameters
| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|:---|
|key|string|The key that identifies the custom property object.|

#### Returns
[CustomProperty](customproperty.md)

### load(param: object)
Fills the proxy object created in JavaScript layer with property and object values specified in the parameter.

#### Syntax
```js
object.load(param);
```

#### Parameters
| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|:---|
|param|object|Optional. Accepts parameter and relationship names as delimited string or an array. Or, provide [loadOption](loadoption.md) object.|

#### Returns
void

### set(key: string, value: object)
Creates or sets a custom property.

#### Syntax
```js
customPropertyCollectionObject.set(key, value);
```

#### Parameters
| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|:---|
|key|string|Required. The custom property's key, which is case-insensitive.|
|value|object|Required. The custom property's value.|

#### Returns
[CustomProperty](customproperty.md)
