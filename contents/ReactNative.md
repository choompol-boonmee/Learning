
========== UI in react-native
https://blog.nativebase.io/getting-started-with-react-native-building-ui-8552dd952589
https://nativebase.io/kitchen-sink-app
https://www.codementor.io/hadaszeilberger/creating-a-user-interface-with-react-native-500nylrhw

========== background task in react-native
https://medium.com/hackernoon/easy-os-background-tasks-in-react-native-bc4476c48b8a
https://www.npmjs.com/package/react-native-background-task
https://blog.expo.io/how-to-run-background-tasks-in-react-native-e1619acef48f
https://stackoverflow.com/questions/35376690/how-can-i-run-background-tasks-in-react-native

========== Push Notification
https://medium.com/@DannyvanderJagt/how-to-use-push-notifications-in-react-native-41e8b14aadae
https://apiko.com/blog/react-native-push-notifications/
https://www.pubnub.com/blog/react-native-push-notifications-ios-android/
https://www.youtube.com/watch?v=PKcfZeZ8yhE
https://www.youtube.com/watch?v=TQmudJLhPx8
https://facebook.github.io/react-native/docs/pushnotificationios
https://www.youtube.com/watch?v=XCk31D5vY0U

========== persistance in react-native
https://pusher.com/tutorials/persisting-data-react-native
https://facebook.github.io/react-native/docs/asyncstorage
https://itnext.io/react-native-why-you-should-be-using-redux-persist-8ad1d68fa48b

======= React-Native tutorials : Academind
https://www.youtube.com/watch?v=qSRrxpdMpVc
https://www.youtube.com/watch?v=6ZnfsJ6mM5c
https://www.youtube.com/watch?v=ojuoYIUmcGg

====== React Native for Wearable
https://blog.teammondrian.com/react-native-for-wearable-bringing-bluetooth-to-javascript/

====== React-Native Technique
https://www.youtube.com/watch?time_continue=325&v=xutPT1oZL2M&feature=emb_logo
https://www.youtube.com/watch?time_continue=9&v=nYkdrAPrdcw&feature=emb_logo
https://egghead.io/lessons/react-redux-store-methods-getstate-dispatch-and-subscribe

====== React-Native Chat
https://css-tricks.com/build-a-chat-app-using-react-hooks-in-100-lines-of-code/

https://getstream.io/chat/react-native-chat/tutorial/
https://www.youtube.com/watch?v=cfggyE1Ptbc
https://www.youtube.com/watch?v=PyNdOCt6i6Q
https://www.youtube.com/watch?v=iKGPXkMcbbY&list=PLYPFxrXyK0ByCS-KG6BZYEoXOkRugZuLD
https://www.youtube.com/watch?v=cU-v9xhhMfM

====== React Native Crash Course
https://www.youtube.com/watch?v=mkualZPRZCs

===== React Tutorial - Learn React - React Crash Course [2019]
https://www.youtube.com/watch?v=Ke90Tje7VS0

===== Node RED
https://www.youtube.com/watch?v=3AR432bguOY&list=PLKYvTRORAnx6a9tETvF95o35mykuysuOw
IPM

codesandbox.io
reactjs.org

nvm install 10.15.3
nvm use 10.15.3

nvm install 12.15.0
nvm use 12.15.0
npx create-react-app my-app

npx create-react-app monsters-rolodex

chrome extension how to
44. Deploy 5:00 => Git Hub
45. React & ReactDOM

yarn list react react-dom react-script
57,58 GitHub
```
yarn add node-sass
git remote add origin git@...
git status
git add -A
git commit -m "SSSSS"
git push origin master
```
66. Routing

```
npx expo-cli init ?
yelp.com/fusion


npm install react-navigation

expo install react-native-gesture-handler react-native-reanimated react-native-screens react-native-safe-area-context @react-native-community/masked-view

npm install react-navigation-stack @react-native-community/masked-view

npm start -c

==== ERROR
rm -r node_modules
rm package-lock.json
expo upgrade
npm start -c

import { createAppContainer } from 'react-navigation';
import { createStackNavigator } from 'react-navigation-stack'

github.com/expo/vector-icons
npm install axios
```

==================================================
===== index.html
<form action="/profile" method="post" enctype="multipart/form-data">
  <input type="file" name="avatar" />
</form>

===== app.jsp
var express = require('express')
var multer  = require('multer')
var upload = multer({ dest: 'uploads/' })
var app = express()
app.post('/profile', upload.single('avatar'), function (req, res, next) {
  // req.file is the `avatar` file
  // req.body will hold the text fields, if there were any
})
==================================================
===== package.json
{
  "name": "file-upload",
  "version": "0.0.1",
  "devDependencies": {
    "express": "^4.12.3",
    "multer": "^0.1.8"
  }
}
===== index.html
```
<!DOCTYPE html>
<html>
<head><meta http-equiv="Content-Type" content="text/html; charset=utf-8">
	<title>Sample File Upload</title>
</head>
<body>
	<form action="/srv06/upload" method="post" enctype="multipart/form-data">
		<input type="file" name="avatar">
		<input type="submit" value="Upload">
	</form>
</body>
</html>
===== app.jsp
var express = require('express');
var multer = require('multer');
var storage = multer.diskStorage({
  destination: function (req, file, cb) {
    cb(null, 'uploads/')
  },
  filename: function (req, file, cb) {
    const uniqueSuffix = Date.now() + '-' + Math.round(Math.random() * 1E9)
    cb(null, file.fieldname + '-' + uniqueSuffix)
  }
})
var upload = multer({ storage: storage })
var app = express();
app.get('/srv06', function(req, res) {
	res.sendFile(__dirname + '/index.html');
});
app.post('/srv06/upload', upload.single('avatar')
	, function (req, res, next) {
	// req.file is the `avatar` file
	// req.body will hold the text fields, if there were any
	res.send(req.body);
	res.send(req.file);
});
app.listen();
```

===== Create a React Native App and Run it on the 
https://egghead.io/lessons/react-native-create-a-react-native-app-and-run-it-on-the-ios-simulator-and-android-emulator

1. ReactNative drawing
https://github.com/terrylinla/react-native-sketch-canvas
https://www.npmjs.com/package/@gigasz/react-native-sketch-canvas
https://www.npmjs.com/package/react-canvas-draw

2. ReactNative share
https://www.npmjs.com/package/react-native-share-menu
https://github.com/react-native-community/react-native-share


