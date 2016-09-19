---
title: Text Bundles
description: Working with text bundles in Node.js
tags: [  tutorial>intermediate, products>sap-hana, products>sap-hana\,-express-edition ]
---
## Prerequisites  
 - **Proficiency:** Intermediate
 - **Tutorials:** [Asynchronous Non-Blocking I/O](http://go.sap.com/developer/tutorials/xsa-node-async.html)

## Next Steps
 - [Web Sockets](http://go.sap.com/developer/tutorials/xsa-node-websockets.html)

## Details
### You will learn  
Working with text bundles in Node.js

### Time to Complete
**15 Min**.

---

1. Return to the Node.js module and the `server.js` source file. 
2. Begin by adding a new Node.js module requirements toward the beginning of the file. For a Node.js module named `./textBundle` which we will create in a moment.
	
	```
	"use strict";
	```

3. Add a route for this module that corresponds to `/node/textBundle` 

	```
	//Create base Express Server App
	```

4. Create a new file in your `js` folder called `textBundle.js`. 

	![new file](4.png)

5. Add the following code to your `textBundle.js` file. It has implemented an HTTP handler for the root URL using express. In the processing of this handler use the `TextBundle` library. When creating a new `TextBundle` instance the input are path (value messages to point to your `message.properties` file) and locale which should call `getLocale` passing in the `req` object. Then write into the `res` object with the `TextBundle` `getText` function (passing in the text ID of greeting and two parameters of `os.hostname()` and `os.type()`. 

	```
	"use strict";
	```

6. Look at the `package.json` file in the editor. You will see the dependencies section which lists all required libraries and their versions. You manually added the `sap-textbundle` and `accept-language-parser` modules to the dependencies section. 

	```
	"dependencies": {
	```

7. You need a few text files to test with. Right mouse click on the `js` folder and choose `Import-> From` File System.  Choose the file `i18n.zip` from the Git repo. Keep all other settings at their default values.  Choose **OK**.

	![import](7.png)

8. We can now run the `js` module. 

	![run](8.png)

9. You should see that the build and deploy was successful. 

	![success](9.png)

10. However if you go to the tab where the service run was started, you will see an 11. Unauthorized message just as in previous sections. This is as intended.

	![unauthoirzed](10.png)

11. So now run the `web` module. 

	![web module](11.png)

12. In the running tab, you should see the `index.html` from earlier.  

	![running tab](12.png)

13. Now change the path in the browser to `/node/textBundle`.  You should see the English message output from your text file in the `i18n` folder. 

	![new path](13.png)

14. In order to test the translated strings, go into the browser Settings. Search for Lang and then choose the Language and input settings button.

	![broswer settings](14.png)

15. Drag and drop to raise German to the top of the list

	![drag drop](15.png)

16. Refresh the web browser and you should now see the German text.

	![refresh](16.png)

17. Repeat the process raising Japanese `[ja]` to the top of the list and refresh the web page

	![new language](17.png)



## Next Steps
 - [Web Sockets](http://go.sap.com/developer/tutorials/xsa-node-websockets.html)