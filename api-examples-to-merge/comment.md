### Getter setter
```js
Excel.run(async (context) => {
    var comment = context.workbook.comments.getItemAt(0);
    comment.content = "new content for the comment";
    return context.sync();
}).catch(function(error) {
	console.log("Error: " + error);
	if (error instanceof OfficeExtension.Error) {
		console.log("Debug info: " + JSON.stringify(error.debugInfo));
	}
});
```

### delete()

```js
Excel.run(async (context) => {
	context.workbook.comments.getItem("{42D7DCA6-8FA5-4CA2-B089-107DFD534F00}").delete();
	return context.sync();
}).catch(function(error) {
	console.log("Error: " + error);
	if (error instanceof OfficeExtension.Error) {
		console.log("Debug info: " + JSON.stringify(error.debugInfo));
	}
});
```
