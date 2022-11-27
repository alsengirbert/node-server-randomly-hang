# nodejs-ramdomly-hung
node server hung, control-c rerumes the node server.

When I use nodejs to run express, I often encount an issue randomly. when I submit a request from my brower, my running node server randomly hung and it doesn't process my request, and my browser can't get response.

I can press control-c to resume the running server, then the running node server will process my request and send response to my browser.

After a long time, I find the issue is not random, it cause by my mistake. Every time I go back to command prompt by left-click somewhere on command prompt. the left-click sometimes will auto-select a white space on command prompt.

the selecting on command prompt will stop processing incoming request until no select status on command prompt. That's why presing control-c can resume the node server to process coming request, because control-c kills select operation on command prompt.

We can also ues right-click on command prompt to resume the node server, because right-click will copy the selected white space, then the selection operation is over, then the node server can proceed to receive request.
