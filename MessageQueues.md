# Message Queues

## Socket.io Chat Example

**1. Explain to a non-technical recruiter what the Chat Example (above) does.**
- The server push messages to clients. Whenever you write a chat message, the idea is that the server will get it and push it to all other connected clients.

**2. What proof of life are we getting on the backend from the above app?**
- listening on the certain port and console messages.

**3. Socket.IO gives us the i0.emit() method to send an event to everyone. What flag would you use if you want to send a message to everyone except for a certain emitting socket?**
- Using broadcast flag along with the socket.broadcast.emit() method.

---

## Rooms
**1. What is a room and how might a room be useful?**
- Room is an arbitrary channel that sockets can join and leave, it can be used to broadcast events to a subset of clients Rooms are a server-only concept (client does not have access to the list of rooms it has joined).

**2. How do you join a room?**
- Can join to subscribe the socket to a given channel socket.join().

**3. How do you leave a room?**
- Can leave the room using socket.leave().

---

## Namespaces
**1. What is a Namespace and what does it allow you to do?**
- A Namespace is a communication channel that allows you to split the logic of your application over a single shared connection (also called "multiplexing").
- 
**2. Each namespace potentially has its own what? (hint: 3 things)**
- Event listeners.
- Middlewares.
- Rooms.
**3. Discuss a possible use case for separate namespaces**
- you want to create a special namespace that only authorized users have access to, so the logic related to those users is separated from the rest of the application.

```
const adminNamespace = io.of("/admin");

adminNamespace.use((socket, next) => {
  // ensure the user has sufficient rights
  next();
});

adminNamespace.on("connection", socket => {
  socket.on("delete user", () => {
    // ...
  });
});
```
- your application has multiple tenants so you want to dynamically create one namespace per tenant.

```
const workspaces = io.of(/^\/\w+$/);

workspaces.on("connection", socket => {
  const workspace = socket.nsp;

  workspace.emit("hello");
});
```

