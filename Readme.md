# ChatBit 💬

A simple real-time chat app I built using React Native (Expo) for frontend and Node.js + Socket.io for backend. It lets two or more users chat with each other instantly, kind of like a mini WhatsApp but way more basic lol.

This was mostly a learning project for me to understand how real-time communication works using websockets, and how frontend and backend actually talk to each other over a network.

## What it does

- User can login with a username and password (currently its dummy login, doesn't check against any real database yet)
- Once logged in, user land on a global chat room
- Messages are sent and recieved in real time using Socket.io
- Shows who joined the room
- Basic UI showing your own messages on right side and others on left, like normal chat apps
- Login session gets saved on device so you don't have to type your name again and again

## Tech used

**Frontend:**
- React Native (Expo)
- Socket.io-client
- React Navigation
- AsyncStorage (for saving login session)

**Backend:**
- Node.js
- Express
- Socket.io

## How to run it

You'll need two terminals open — one for backend, one for frontend.

### Backend
```bash
cd chat-app-backend
npm install
node server.js
```
It should say "Running on port 5000" if it worked.

### Frontend
```bash
cd chat-app-frontend
npm install
npx expo start
```
Scan the QR code with Expo Go app on your phone.

**Important:** in `App.js`, there's a variable called `SOCKET_URL`. If your testing on a real phone, you need to change `localhost` to your computer's actual local IP address (something like `192.168.1.35`), otherwise the app won't be able to connect to backend. You can find your IP using `ipconfig` command in terminal.

## Known issues / things I still wanna fix

- No real database yet, so login is fake and messages don't get saved anywhere (once you close app, chat history is gone)
- Only one global room right now, no private chats or multiple rooms
- No image/file sharing, just text messages for now

## Why I made this

Wanted to actually understand how apps like WhatsApp handle real time messaging under the hood, instead of just using some library and copy pasting code without knowing whats happening. Learned a lot about socket connections, react native navigation, and debugging really annoying dependency version errors lol.

---

Made by Rahul Dev