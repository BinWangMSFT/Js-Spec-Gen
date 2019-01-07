# CommentCollection


### add(content: string, cellAddress: string, contentType: contentType)

```js

Excel.run(async (context) => {

    var range = context.workbook.getSelectedRange();
    context.workbook.comments.add("text of the comment", range);
    await context.sync();
}).catch(function(error) {
		console.log("Error: " + error);
		if (error instanceof OfficeExtension.Error) {
			console.log("Debug info: " + JSON.stringify(error.debugInfo));
		}
});
```
### Getter setter
```js
Excel.run(async (context) => {
    var comment = context.workbook.comments.getItemAt(0);
    comment.content = "new content for the comment";
    await context.sync();

}).catch(function(error) {
		console.log("Error: " + error);
		if (error instanceof OfficeExtension.Error) {
			console.log("Debug info: " + JSON.stringify(error.debugInfo));
		}
});
```
