async function sendMessage() {
  const userInput = document.getElementById("user-input").value;
  if (!userInput) return;

  // Hiển thị tin nhắn của người dùng
  const messagesDiv = document.getElementById("messages");
  const userMessage = document.createElement("div");
  userMessage.textContent = "You: " + userInput;
  messagesDiv.appendChild(userMessage);

  // Gửi yêu cầu đến server AI
  const response = await fetch("/chat", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify({ message: userInput })
  });

  const data = await response.json();

  // Hiển thị phản hồi từ AI
  const botMessage = document.createElement("div");
  botMessage.textContent = "AI: " + data.reply;
  messagesDiv.appendChild(botMessage);

  // Xóa input
  document.getElementById("user-input").value = "";
}
