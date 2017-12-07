# Redactor fixes

Based on Redactor 10.2.2 retrieved from [OsTicket 1.10.1](https://github.com/osTicket/osTicket)

Fix two bugs:
* Image paste (copy/printscreen/etc) didn't work with error: `The given range isn't in document.`
* When pasting repeatedly very fast, there were bits of Redactor markup left on the HTML `<span class="redactor-invisible-space"></span>`, which would break Enter key normal behavior

### Samples

* redactor.original.html: shows original behavior (you can't paste images and new line doesn't work correctly)
* redactor.fixed.html: pasting an image works correctly (wherever you paste it) and new line works after pasting

### Limitations

Images pasted on the editor area are saved as data URIs (base64 encoded). It wasn't tested for saving the image on server side.