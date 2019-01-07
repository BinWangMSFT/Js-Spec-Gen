# CommentCollection


### add(content: string, cellAddress: string, contentType: contentType)

```js

Excel.run(async (context) => {
    var range = context.workbook.getSelectedRange();
    context.workbook.comments.add("text of the comment", range);
	return context.sync();
}).catch(function(error) {
	console.log("Error: " + error);
	if (error instanceof OfficeExtension.Error) {
		console.log("Debug info: " + JSON.stringify(error.debugInfo));
	}
});
```
