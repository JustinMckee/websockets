# websockets

To get these examples running:
1. `$ cd server`
2. `$ npm install`
3. `$ node index.js` to run the websocket server

## See connections & disconnections to the server in your terminal

- `$ New client connected!` displays for every new connection.
- `$ Client has disconnected.` displays for every disconnection.

## Send your message to the server and get it back in ALL CAPS.

- Add your message in the input field.
- Click "Send"
- See your transformed message sent from the server.
- Look at your dev tools console to see the MessageEvent object.

## See network requests in your browser's network tab

- Open DevTools.
- Click on "Network".
- Click on "WS" for the websocket connection type.
- Open index.html in your browser and you will see a request to "localhost".
- Click on "localhost" and view "Messages" tab to see requests and responses.

## How it works

1. Browser sends an http request... but then it is upgraded to websocket connection.
2. In the "Request Headers" you can see "Connection: upgrade" and "Upgrade: websocket".
3. The "Response Headers" sent by server say "Connection: Upgrade" and "Upgrade: websocket".
4. The handshake is complete and data can be sent back-and-forth
