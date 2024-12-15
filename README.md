<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AI Chat</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; padding: 0; }
    #chat-container { max-width: 600px; margin: 50px auto; border: 1px solid #ccc; border-radius: 8px; padding: 10px; background-color: #f9f9f9; }
    #messages { height: 400px; overflow-y: auto; margin-bottom: 10px; }
    #input-area { display: flex; }
    #user-input { flex: 1; padding: 10px; border: 1px solid #ccc; border-radius: 4px; }
    #send-button { padding: 10px; background-color: #007bff; color: white; border: none; border-radius: 4px; margin-left: 5px; cursor: pointer; }
  </style>
</head>
<body>
  <div id="chat-container">
    <div id="messages"></div>
    <div id="input-area">
      <input id="user-input" type="text" placeholder="Type your message here...">
      <button id="send-button" onclick="sendMessage()">Send</button>
    </div>
  </div>

  <script src="chat.js"></script>
</body>
</html>
