*Help avoid duplicate issue reports, check [existing issues](https://github.com/QuickBlox/quickblox-javascript-sdk/issues)*

**Environment details**
*(Operating system, browser information, SDK version)*
Operating system : Windows
Browser : google chrome
SDK version: 2.3.3 (javascript)

**Did this work before?**
NO

**Expected behavior**
How to send custom parameters with in message(send/receive) from web application to android and ios mobile client

**Actual behavior**
Not able to send custom parameters with message(send/receive)

**Logs**
*(please, switch on a [debugging mode](http://quickblox.com/developers/Javascript#Configuration) and share us outputs uses github [gist](https://gist.github.com/))*


**Steps to reproduce the behavior**
we are using sendMessage function

function sendMessage(text, attachmentFileId, fileType) {

--> We need to pass some extra parameters from this function.
var msg = {
    type: currentDialog.type === 3 ? 'chat' : 'groupchat',
    body: text,
    extension: {
        save_to_history: 1 //,

    },
    JobName: 'Test Job',
    JobLocation: 'Hyderabad',
    Compatibility: '80',
    JobId: '1212',
    senderId: currentUser.id,
    markable: 1
};

**Any others comments?**
We can able to pass information with Web application to web application by changing following code 

var msg = {
    type: currentDialog.type === 3 ? 'chat' : 'groupchat',
    body: text,
    extension: {
        save_to_history: 1 //,

   
    JobName: 'Test Job',
    JobLocation: 'Hyderabad',
    Compatibility: '80',
    JobId: '1212',
    senderId: currentUser.id,
    markable: 1
     },
};

Bur this is receivable in android and ios mobile client

We raised ticket on quickblox support site:
[Quickblox Ticket #33008]: Not able send custom parameters with message(send/receive)


