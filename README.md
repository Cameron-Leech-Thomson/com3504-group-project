# COM3504 - The Intelligent Web - Group Project

# Self-Assessment & System Breakdown
## Web App
Overall, everything that has been implemented works though there are a few features missing from the solution. The service worker follows the cache then network model. It provides fast accessible content whilst keeping it relatively up to date. When offline, new reports made are stored locally and then pushed to mongo when back online. Everytime you enter a room a chat is initiated and whatever is said is stored in indexedDB. These chats can then be viewed again at a later date. 

## NodeJS Server
All of the data being communicated is done correctly between the client and server. It also sends the data correctly to the MongoDB. The image however is not sent as the correct type, it is sent as a string storing its URL rather than as an image file. JSON is used in parts of the solution to send errors back but it is not used in many other areas. The routes are organised pretty effectively making use of controllers.

## MongoDB
The database stores the title of the report, as well as the author, the description, the date-time it was made, and the URL of the image. The database does not store the image file itself. The database syncs with IndexedDB by sending all of the cached data to the server's database if it is not already stored, allowing the user to create reports while offline. 

## Client-Server Communication (Axios + Socket.io)
Socket.io is used to emit the chat messages between all users currently subscribed to that particular chat room. Axios is used to send the locally stored reports once the user goes online.

## Swagger Documentation
More comments and JavaDocs would be required to call the standard of code documentation appropriate. The swagger documentation is of good quality, and explains the results of the various actions that the user can perform.

## Authors
Below are the contributors, as well as their contributions. Please note that these are not *solely* the only contributions made, and there was plenty of cross-collaboration where it was beneficial.
- Kieran Powell:
    - MongoDB
    - IndexedDB
    - Axios
    - NodeJS
- Cameron Leech-Thomson
    - Socket.io
    - Google Knowledge Graph
    - Chatrooms
    - NodeJS
- Connor Mitchell
    - Service Worker
    - Create/Display Reports
    - Swagger Docs
    - NodeJS
