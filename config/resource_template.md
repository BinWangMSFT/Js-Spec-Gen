<header>
# %name% resource type
%description%
</header>

<extendedremarks>
%remarks%
</extendedremarks> 

<requirements>
## Requirement set and supported hosts

| Requirement set | Application	|
|:---------------|:--------|
|%req%|%apps%|

</requirements>

<properties>
### Properties

| Property	   | Type	| Description| Req. Set Ver#| 
|:-------------|:-------|:-----------|:---|
>r|%name%      | %type% | %description% | %req% |

%propertygetset%
%propertynotes%
</properties>
<relationships>
### Relationships
| Relationship | Type	| Description| Requirement Set|
|:-------------|:-------|:-----------|:---|
>r|%name%      | [%type%](%link%) | %description% | %req% |

%relationshipnotes%
</relationships>

<methods>

## Methods

| Method	   | Return Type    | Description | Requirement Set|
|:-------------|:---------------|:------------|:----|
>r| [%name%](%link%)     | %dtype% | %description% | %req%|

%methodnotes%

## Method Details

<api>
### %apisignature%
%apidescription%
%syntax%
<parameter>
#### Parameters
%noparam%
| Method	   | Type    | Description | 
|:-------------|:---------------|:------------|
>r| %name%     | %dtype% | %description% | 

</parameter>
#### Returns
%returntype% 

<example>
#### Example
%examplelines%
</example>

</api>

</methods>