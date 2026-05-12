# genlayer-ai-moderated-chat
ai-native-chat-rooms/
├── index.html
├── style.css
├── script.js
├── assets/
│   └── logo.png (optional)
└── README.md
index.html
<!DOCTYPE html>
<html lang="en" class="dark">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>GenChat • AI-Native Moderated Rooms</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="style.css" />
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css" rel="stylesheet">
</head>
<body class="bg-gray-950 text-white font-sans">

  <!-- Hero -->
  <section class="min-h-screen flex items-center justify-center relative overflow-hidden">
    <div class="absolute inset-0 bg-gradient-to-br from-purple-600/20 to-cyan-500/20"></div>
    <div class="max-w-5xl mx-auto text-center px-6 relative z-10">
      <h1 class="text-6xl md:text-7xl font-bold mb-6 bg-gradient-to-r from-purple-400 to-cyan-400 bg-clip-text text-transparent">
        AI-Native Chat Rooms
      </h1>
      <p class="text-2xl md:text-3xl mb-8 text-gray-300">
        Decentralized. Auto-moderated.<br>Powered by <span class="text-cyan-400">GenLayer Intelligent Contracts</span>
      </p>
      <div class="flex justify-center gap-4">
        <a href="#demo" class="px-8 py-4 bg-white text-black font-semibold rounded-2xl hover:bg-cyan-400 transition">
          Try Demo
        </a>
        <a href="https://genlayer.com" target="_blank" class="px-8 py-4 border border-white/50 hover:border-white rounded-2xl transition">
          Learn GenLayer →
        </a>
      </div>
      <p class="mt-6 text-sm text-gray-400">Deployed with wallet • Messages on-chain • AI judges everything</p>
    </div>
  </section>

  <!-- Features -->
  <section class="py-20 bg-black/50">
    <div class="max-w-6xl mx-auto px-6">
      <h2 class="text-4xl font-bold text-center mb-12">Why This Works</h2>
      <div class="grid md:grid-cols-3 gap-8">
        <div class="bg-gray-900 p-8 rounded-3xl">
          <i class="fa-solid fa-robot text-4xl text-purple-400 mb-4"></i>
          <h3 class="text-xl font-semibold mb-3">Intelligent Moderation</h3>
          <p class="text-gray-400">AI detects spam, toxicity, scams using natural language. Dynamic rules like “Ban scam promoters” enforced on-chain.</p>
        </div>
        <div class="bg-gray-900 p-8 rounded-3xl">
          <i class="fa-solid fa-globe text-4xl text-cyan-400 mb-4"></i>
          <h3 class="text-xl font-semibold mb-3">Live Web Context</h3>
          <p class="text-gray-400">Contract fetches real-time data to verify claims in debates. No oracles needed.</p>
        </div>
        <div class="bg-gray-900 p-8 rounded-3xl">
          <i class="fa-solid fa-trophy text-4xl text-yellow-400 mb-4"></i>
          <h3 class="text-xl font-semibold mb-3">Reward System</h3>
          <p class="text-gray-400">Helpful users get auto-minted tokens. Toxic behavior gets slashed.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- How it Works -->
  <section class="py-20">
    <div class="max-w-5xl mx-auto px-6">
      <h2 class="text-4xl font-bold text-center mb-12">How It Works</h2>
      <div class="space-y-12">
        <div class="flex flex-col md:flex-row gap-8 items-center">
          <div class="md:w-1/2">
            <div class="bg-gray-900 p-6 rounded-2xl text-sm font-mono text-green-400">1. Create Room</div>
            <p class="mt-4 text-gray-400">Connect wallet → Deploy public/private room with custom rules in natural language.</p>
          </div>
          <div class="md:w-1/2">
            <div class="bg-gray-900 p-6 rounded-2xl text-sm font-mono text-cyan-400">2. Post Message</div>
            <p class="mt-4 text-gray-400">Message is sent to the Intelligent Contract.</p>
          </div>
          <div class="md:w-1/2">
            <div class="bg-gray-900 p-6 rounded-2xl text-sm font-mono text-purple-400">3. AI Evaluates</div>
            <p class="mt-4 text-gray-400">Validators run diverse LLMs → Reach consensus → Auto-moderate + reward.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Live Demo -->
  <section id="demo" class="py-20 bg-black/70">
    <div class="max-w-4xl mx-auto px-6">
      <h2 class="text-4xl font-bold text-center mb-8">Live Mock Demo</h2>
      <div class="bg-gray-900 rounded-3xl p-6 border border-gray-700">
        <div class="flex justify-between mb-4 text-sm">
          <div><span class="text-purple-400">🔴</span> Debate Room: Crypto Regulation</div>
          <div class="text-green-400">12 online</div>
        </div>
        <div id="chat" class="h-96 overflow-y-auto space-y-4 p-4 bg-black/50 rounded-2xl mb-4 text-sm"></div>
        
        <div class="flex gap-3">
          <input id="msgInput" type="text" placeholder="Type a message..." 
                 class="flex-1 bg-gray-800 rounded-2xl px-5 py-3 focus:outline-none focus:ring-2 focus:ring-cyan-400">
          <button onclick="sendMessage()" 
                  class="px-8 bg-cyan-500 hover:bg-cyan-400 text-black font-semibold rounded-2xl transition">
            Send
          </button>
        </div>
        <p class="text-[10px] text-center mt-3 text-gray-500">This is a frontend demo. Real version runs on GenLayer testnet.</p>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="py-12 border-t border-gray-800">
    <div class="max-w-6xl mx-auto px-6 text-center text-gray-400 text-sm">
      <p>Built for <span class="text-cyan-400">GenLayer</span> • Intelligent Contracts</p>
      <p class="mt-2">Open Source • Deployed on GitHub Pages</p>
    </div>
  </footer>

  <script src="script.js"></script>
</body>
</html>
style.css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

body {
  font-family: 'Inter', system-ui, sans-serif;
}

.chat-message {
  animation: fadeIn 0.3s ease;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}
script.js
function sendMessage() {
  const input = document.getElementById('msgInput');
  const chat = document.getElementById('chat');
  if (!input.value.trim()) return;

  const msg = document.createElement('div');
  msg.className = 'chat-message flex gap-3';
  msg.innerHTML = `
    <div class="w-8 h-8 bg-gradient-to-br from-purple-500 to-cyan-500 rounded-full flex-shrink-0"></div>
    <div>
      <div class="text-xs text-gray-500">@you • just now</div>
      <div class="bg-gray-800 px-4 py-3 rounded-2xl rounded-tl-none">
        ${input.value}
      </div>
      <div class="text-[10px] text-green-400 mt-1">✓ AI Approved • +5 rep</div>
    </div>
  `;
  chat.appendChild(msg);
  chat.scrollTop = chat.scrollHeight;
  input.value = '';

  // Simulate moderation
  setTimeout(() => {
    if (Math.random() > 0.7) {
      const mod = document.createElement('div');
      mod.className = 'text-center text-xs text-yellow-400 py-2';
      mod.textContent = 'AI Moderator: Message flagged as potentially misleading';
      chat.appendChild(mod);
      chat.scrollTop = chat.scrollHeight;
    }
  }, 800);
}

// Auto demo messages
setTimeout(() => {
  const chat = document.getElementById('chat');
  const welcome = document.createElement('div');
  welcome.innerHTML = `
    <div class="text-center text-xs text-gray-500 py-2">Room started • AI rules active</div>
  `;
  chat.appendChild(welcome);
}, 500);
