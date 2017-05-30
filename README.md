## RCTMessageUI

React native bridge to MessageUI.framework

## Installation
Install via npm :
`npm install RCTMessageUI`

Now you need to link the native library to your current project, you can do that manually
by placing the .a lib into your project but we recommend you to use `rnpm` because it will
handle iOS and Android libraries for you and it's pretty straight forward

```

$npm install rnpm -g

$rnpm link

```

rnpm link will link all dependencies automatically but you will still need to re-build the native app

### Usage
!!! important: it will not work in the iOS Simulator, works only on real device


```javascript
import {MessageUI} from 'RCTMessageUI';

MessageUI.showMessageComposeWithOptions(
            {
                body                   : 'Ana are mere',
                recipients             : ['11211241', 'b@bb.bbb'],
                disableUserAttachments : true
            }, (error, messageComposeResult) => {
                if (error) {
                    console.error(error);
                } else {
                    alert('mailComposeResult : ' + messageComposeResult);
                }
            });
```
