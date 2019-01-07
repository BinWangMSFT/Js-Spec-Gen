

### Getter setter

Get a comment reply and change the content

```js
Excel.run(async (context) => {

    var comment = context.workbook.comments.getItemByReplyID("{42D7DCA6-8FA5-4CA2-B089-107DFD534F00}");
    context.load(comment);
    return context.sync();

    var reply = comment.replies.getItem("{42D7DCA6-8FA5-4CA2-B089-107DFD534F00}");
    reply.content = "new content for the reply";
    return context.sync();

}).catch(function(error) {
		console.log("Error: " + error);
		if (error instanceof OfficeExtension.Error) {
			console.log("Debug info: " + JSON.stringify(error.debugInfo));
		}
});
```
### delete()

Delete a comment reply given reply ID

```js
Excel.run(async (context) => {

        var comment = context.workbook.comments.getItemByReplyID("{42D7DCA6-8FA5-4CA2-B089-107DFD534F00}");
        context.load(comment);
        return context.sync();

        comment.replies.getItem("{42D7DCA6-8FA5-4CA2-B089-107DFD534F00}").delete();
        return context.sync();
});.catch(function(error) {
    console.log("Error: " + error);
    if (error instanceof OfficeExtension.Error) {
        console.log("Debug info: " + JSON.stringify(error.debugInfo));
    }
});
```
