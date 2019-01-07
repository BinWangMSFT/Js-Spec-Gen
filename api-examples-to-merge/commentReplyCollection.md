### add(content: string, contentType: contentType)
```js
Excel.run(async (context) => {
        var comment = context.workbook.comments.getItemByCell("sheet1!A1");
        context.load(comment);
        return context.sync();

        comment.replies.add("text of the reply");
        return context.sync();
    }).catch(function(error) {
		console.log("Error: " + error);
		if (error instanceof OfficeExtension.Error) {
			console.log("Debug info: " + JSON.stringify(error.debugInfo));
		}
});
```