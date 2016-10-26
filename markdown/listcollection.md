# ListCollection Object (JavaScript API for Word)

_Word 2016, Word for iPad, Word for Mac, Word Online_

Contains a collection of [list](list.md) objects.

## Properties

| Property	   | Type	|Description| Req. Set|
|:---------------|:--------|:----------|:----|
|items|[List[]](list.md)|A collection of list objects. Read-only.|[1.3](../reqset/word-requirement.md)|

_See property access [examples.](#property-access-examples)_

## Relationships
None


## Methods

| Method		   | Return Type	|Description| Req. Set|
|:---------------|:--------|:----------|:----|
|[getById(id: number)](#getbyidid-number)|[List](list.md)|Gets a list by its identifier.|[1.3](../reqset/word-requirement.md)|
|[getFirst()](#getfirst)|[List](list.md)|Gets the first list in this collection.|[1.3](../reqset/word-requirement.md)|
|[getItem(index: number)](#getitemindex-number)|[List](list.md)|Gets a list object by its index in the collection.|[1.3](../reqset/word-requirement.md)|
|[load(param: object)](#loadparam-object)|void|Fills the proxy object created in JavaScript layer with property and object values specified in the parameter.|[1.1](../reqset/word-requirement.md)|

## Method Details


### getById(id: number)
Gets a list by its identifier.

#### Syntax
```js
listCollectionObject.getById(id);
```

#### Parameters
| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|:---|
|id|number|Required. A list identifier.|

#### Returns
[List](list.md)

### getFirst()
Gets the first list in this collection.

#### Syntax
```js
listCollectionObject.getFirst();
```

#### Parameters
None

#### Returns
[List](list.md)

### getItem(index: number)
Gets a list object by its index in the collection.

#### Syntax
```js
listCollectionObject.getItem(index);
```

#### Parameters
| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|:---|
|index|number|A number that identifies the index location of a list object.|

#### Returns
[List](list.md)

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
