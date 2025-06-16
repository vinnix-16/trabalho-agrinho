<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Agrinho 2025 - Festa do Campo e Cidade</title>
    <link rel="stylesheet" href="styles.css" />
</head>
<body>
    <header>
        <h1>Agrinho 2025</h1>
        <h2>Celebrando a união do Campo e da Cidade</h2>
    </header>

    <section class="intro">
        <p>Venha participar de uma festa que celebra a riqueza do nosso campo e a alegria da nossa cidade! Prepare-se para atividades, música, comidas típicas e muita diversão!</p>
    </section>

    <section class="carousel">
        <h3>Imagens do Campo e da Cidade</h3>
        <div class="images-container">
            <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Campo" class="slide" />
            <img src="https://images.unsplash.com/photo-1503457574464-8184d0592c9c?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Cidade" class="slide" />
        </div>
        <button id="prevBtn">Anterior</button>
        <button id="nextBtn">Próximo</button>
    </section>

    <section class="programa">
        <h3>Programação</h3>
        <ul>
            <li><strong>09h:</strong> Abertura com música ao vivo</li>
            <li><strong>10h:</strong> Oficina de artes do campo</li>
            <li><strong>12h:</strong> Almoço típico</li>
            <li><strong>14h:</strong> Show de talentos urbanos e rurais</li>
            <li><strong>16h:</strong> Feira de produtos locais</li>
            <li><strong>18h:</strong> Encerramento com shows e queima de fogos</li>
        </ul>
    </section>

    <section class="participe">
        <h3>Participe!</h3>
        <p>Quer deixar sua mensagem ou contar sua história? Clique no botão abaixo:</p>
        <button id="messageBtn">Deixe sua mensagem</button>
        <div id="messageBox" class="hidden">
            <textarea id="userMessage" rows="4" cols="50" placeholder="Sua mensagem..."></textarea>
            <button id="sendMessage">Enviar</button>
        </div>
        <div id="messagesList"></div>
    </section>

    <footer>
        <p>&copy; 2025 Agrinho - Festa do Campo e Cidade</p>
    </footer>// Controle de slideshow de imagens
const slides = document.querySelectorAll('.slide');
const prevBtn = document.getElementById('prevBtn');
const nextBtn = document.getElementById('nextBtn');
let currentSlide = 0;

// Função para mostrar slide
function showSlide(index) {
    slides.forEach((slide, i) => {
        slide.classList.toggle('active', i === index);
    });
}

// Mostrar o primeiro slide ao carregar
showSlide(currentSlide);

// Eventos dos botões
prevBtn.addEventListener('click', () => {
    currentSlide = (currentSlide - 1 + slides.length) % slides.length;
    showSlide(currentSlide);
});

nextBtn.addEventListener('click', () => {
    currentSlide = (currentSlide + 1) % slides.length;
    showSlide(currentSlide);
});

// Interatividade de mensagens
const messageBtn = document.getElementById('messageBtn');
const messageBox = document.getElementById('messageBox');
const sendMessageBtn = document.getElementById('sendMessage');
const userMessageInput = document.getElementById('userMessage');
const messagesList = document.getElementById('messagesList');

messageBtn.addEventListener('click', () => {
    messageBox.classList.toggle('hidden');
});

sendMessageBtn.addEventListener('click', () => {
    const message = userMessageInput.value.trim();
    if (message) {
        const messageElement = document.createElement('p');
        messageElement.textContent = message;
        messagesList.appendChild(messageElement);
        userMessageInput.value = '';
        alert('Mensagem enviada! Obrigado por participar.');
        messageBox.classList.add('hidden');
    } else {
        alert('Por favor, escreva sua mensagem primeiro.');
    }
});


    <script src="script.js"></script>
</body>
</html>trong> Encerramento com shows e queima de fogos</li>
        </ul>
    </section>
    body {
    font-family: Arial, sans-serif;
    background-color: #f0f8f0;
    margin: 0;
    padding: 0;
    color: #333;
}

header {
    background-color: #4CAF50;
    color: white;
    padding: 20px;
    text-align: center;
}

h1 {
    margin: 0;
    font-size: 2.5em;// Controle de slideshow de imagens
const slides = document.querySelectorAll('.slide');
const prevBtn = document.getElementById('prevBtn');
const nextBtn = document.getElementById('nextBtn');
let currentSlide = 0;

// Função para mostrar slide
function showSlide(index) {
    slides.forEach((slide, i) => {
        slide.classList.toggle('active', i === index);
    });
}

// Mostrar o primeiro slide ao carregar
showSlide(currentSlide);

// Eventos dos botões
prevBtn.addEventListener('click', () => {
    currentSlide = (currentSlide - 1 + slides.length) % slides.length;
    showSlide(currentSlide);
});

nextBtn.addEventListener('click', () => {
    currentSlide = (currentSlide + 1) % slides.length;
    showSlide(currentSlide);
});

// Interatividade de mensagens
const messageBtn = document.getElementById('messageBtn');
const messageBox = document.getElementById('messageBox');
const sendMessageBtn = document.getElementById('sendMessage');
const userMessageInput = document.getElementById('userMessage');
const messagesList = document.getElementById('messagesList');

messageBtn.addEventListener('click', () => {
    messageBox.classList.toggle('hidden');
});

sendMessageBtn.addEventListener('click', () => {
    const message = userMessageInput.value.trim();
    if (message) {
        const messageElement = document.createElement('p');
        messageElement.textContent = message;
        messagesList.appendChild(messageElement);
        userMessageInput.value = '';
        alert('Mensagem enviada! Obrigado por participar.');
        messageBox.classList.add('hidden');
    } else {
        alert('Por favor, escreva sua mensagem primeiro.');
    }
});

}

h2 {
    margin: 10px 0 0 0;
    font-weight: normal;
}

section {
    padding: 20px;
    margin: 10px;
    background-color: #ffffff;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

.carousel {
    text-align: center;
}

.images-container {
    position: relative;
    width: 100%;
    max-width: 600px;
    margin: 0 auto;
    overflow: hidden;
}

.slide {
    width: 100%;
    display: none;
    border-radius: 8px;
}

.slide.active {
    display: block;
}

button {
    margin: 10px;// Controle de slideshow de imagens
const slides = document.querySelectorAll('.slide');
const prevBtn = document.getElementById('prevBtn');
const nextBtn = document.getElementById('nextBtn');
let currentSlide = 0;

// Função para mostrar slide
function showSlide(index) {
    slides.forEach((slide, i) => {
        slide.classList.toggle('active', i === index);
    });
}

// Mostrar o primeiro slide ao carregar
showSlide(currentSlide);

// Eventos dos botões
prevBtn.addEventListener('click', () => {
    currentSlide = (currentSlide - 1 + slides.length) % slides.length;
    showSlide(currentSlide);
});

nextBtn.addEventListener('click', () => {
    currentSlide = (currentSlide + 1) % slides.length;
    showSlide(currentSlide);
});

// Interatividade de mensagens
const messageBtn = document.getElementById('messageBtn');
const messageBox = document.getElementById('messageBox');
const sendMessageBtn = document.getElementById('sendMessage');
const userMessageInput = document.getElementById('userMessage');
const messagesList = document.getElementById('messagesList');

messageBtn.addEventListener('click', () => {
    messageBox.classList.toggle('hidden');
});

sendMessageBtn.addEventListener('click', () => {
    const message = userMessageInput.value.trim();
    if (message) {
        const messageElement = document.createElement('p');
        messageElement.textContent = message;
        messagesList.appendChild(messageElement);
        userMessageInput.value = '';
        alert('Mensagem enviada! Obrigado por participar.');
        messageBox.classList.add('hidden');
    } else {
        alert('Por favor, escreva sua mensagem primeiro.');
    }
});

    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 1em;
}

button:hover {
    background-color: #45a049;
}

#messageBox {
    margin-top: 10px;
}// Controle de slideshow de imagens
const slides = document.querySelectorAll('.slide');
const prevBtn = document.getElementById('prevBtn');
const nextBtn = document.getElementById('nextBtn');
let currentSlide = 0;

// Função para mostrar slide
function showSlide(index) {
    slides.forEach((slide, i) => {
        slide.classList.toggle('active', i === index);
    });
}

// Mostrar o primeiro slide ao carregar
showSlide(currentSlide);

// Eventos dos botões
prevBtn.addEventListener('click', () => {
    currentSlide = (currentSlide - 1 + slides.length) % slides.length;
    showSlide(currentSlide);
});

nextBtn.addEventListener('click', () => {
    currentSlide = (currentSlide + 1) % slides.length;
    showSlide(currentSlide);
});

// Interatividade de mensagens
const messageBtn = document.getElementById('messageBtn');
const messageBox = document.getElementById('messageBox');
const sendMessageBtn = document.getElementById('sendMessage');
const userMessageInput = document.getElementById('userMessage');
const messagesList = // Controle de slideshow de imagens
const slides = document.querySelectorAll('.slide');
const prevBtn = document.getElementById('prevBtn');
const nextBtn = document.getElementById('nextBtn');
let currentSlide = 0;

// Função para mostrar slide
function showSlide(index) {
    slides.forEach((slide, i) => {
        slide.classList.toggle('active', i === index);
    });// Controle de slideshow de imagens
const slides = document.querySelectorAll('.slide');
const prevBtn = document.getElementById('prevBtn');
const nextBtn = document.getElementById('nextBtn');
let currentSlide = 0;

// Função para mostrar slide
function showSlide(index) {
    slides.forEach((slide, i) => {
        slide.classList.toggle('active', i === index);
    });
}

// Mostrar o primeiro slide ao carregar
showSlide(currentSlide);

// Eventos dos botões
prevBtn.addEventListener('click', () => {
    currentSlide = (currentSlide - 1 + slides.length) % slides.length;
    showSlide(currentSlide);
});

nextBtn.addEventListener('click', () => {
    currentSlide = (currentSlide + 1) % slides.length;
    showSlide(currentSlide);
});

// Interatividade de mensagens
const messageBtn = document.getElementById('messageBtn');
const messageBox = document.getElementById('messageBox');
const sendMessageBtn = document.getElementById('sendMessage');
const userMessageInput = document.getElementById('userMessage');
const messagesList = document.getElementById('messagesList');

messageBtn.addEventListener('click', () => {
    messageBox.classList.toggle('hidden');
});

sendMessageBtn.addEventListener('click', () => {
    const message = userMessageInput.value.trim();
    if (message) {
        const messageElement = document.createElement('p');
        messageElement.textContent = message;
        messagesList.appendChild(messageElement);
        userMessageInput.value = '';
        alert('Mensagem enviada! Obrigado por participar.');
        messageBox.classList.add('hidden');
    } else {
        alert('Por favor, escreva sua mensagem primeiro.');
    }
});

}

// Mostrar o primeiro slide ao carregar
showSlide(currentSl// Controle de slideshow de imagens
const slides = document.querySelectorAll('.slide');
const prevBtn = document.getElementById('prevBtn');
const nextBtn = document.getElementById('nextBtn');
let currentSlide = 0;

// Função para mostrar slide
function showSlide(index) {
    slides.forEach((slide, i) => {
        slide.classList.toggle('active', i === index);
    });
}

// Mostrar o primeiro slide ao carregar
showSlide(currentSlide);

// Eventos dos botões
prevBtn.addEventListener('click', () => {
    currentSlide = (currentSlide - 1 + slides.length) % slides.length;
    showSlide(currentSlide);
});

nextBtn.addEventListener('click', () => {
    currentSlide = (currentSlide + 1) % slides.length;
    showSlide(currentSlide);
});

// Interatividade de mensagens
const messageBtn = document.getElementById('messageBtn');
const messageBox = document.getElementById('messageBox');
const sendMessageBtn = document.getElementById('sendMessage');
const userMessageInput = document.getElementById('userMessage');
const messagesList = document.getElementById('messagesList');

messageBtn.addEventListener('click', () => {
    messageBox.classList.toggle('hidden');
});

sendMessageBtn.addEventListener('click', () => {
    const message = userMessageInput.value.trim();
    if (message) {
        const messageElement = document.createElement('p');
        messageElement.textContent = message;
        messagesList.appendChild(messageElement);
        userMessageInput.value = '';
        alert('Mensagem enviada! Obrigado por participar.');
        messageBox.classList.add('hidden');
    } else {
        alert('Por favor, escreva sua mensagem primeiro.');
    }
});
ide);

// Eventos dos botões
prevBtn.addEventListener('click', () => {
    currentSlide = (currentSlide - 1 + slides.length) % slides.length;
    showSlide(currentSlide);
});

nextBtn.addEventListener('click', () => {
    currentSlide = (currentSlide + 1) % slides.length;
    showSlide(currentSlide);
});

// Interatividade de mensagens
const messageBtn = document.getElementById('messageBtn');
const messageBox = document.getElementById('messageBox');
const sendMessageBtn = document.getElementById('sendMessage');
const userMessageInput = document.getElementById('userMessage');
const messagesList = document.getElementById('messagesList');

messageBtn.addEventListener('click', () => {
    messageBox.classList.toggle('hidden');
});

sendMessageBtn.addEventListener('click', () => {
    const message = userMessageInput.value.trim();
    if (message) {
        const messageElement = document.createElement('p');
        messageElement.textContent = message;
        messagesList.appendChild(messageElement);
        userMessageInput.value = '';
        alert('Mensagem enviada! Obrigado por participar.');
        messageBox.classList.add('hidden');
    } else {
        alert('Por favor, escreva sua mensagem primeiro.');
    }
});
document.getElementById('messagesList');

messageBtn.addEventListener('click', () => {
    messageBox.classList.toggle('hidden');
});

sendMessageBtn.addEventListener('click', () => {
    const message = userMessageInput.value.trim();
    if (message) {
        const messageElement = document.createElement('p');
        messageElement.textContent = message;
        messagesList.appendChild(messageElement);
        userMessageInput.value = '';
        alert('Mensagem enviada! Obrigado por participar.');
        messageBox.classList.add('hidden');
    } else {
        alert('Por favor, escreva sua mensagem primeiro.');
    }
});


.hidden {
    display: none;
}

#messagesList {
    margin-top: 20px;
    background-color: #e0f7fa;
    padding: 10px;
    border-radius: 8px;
}

footer {
    background-color: #4CAF50;
    color: white;
    text-align: center;
    padding: 10px;
}

/* Responsividade */
@media(max-width: 700px) {
    body {
        font-size: 14px;
    }
    button {
        padding: 8px 16px;
        font-size: 0.9em;
    }
}
// Controle de slideshow de imagens
const slides = document.querySelectorAll('.slide');
const prevBtn = document.getElementById('prevBtn');
const nextBtn = document.getElementById('nextBtn');
let currentSlide = 0;

// Função para mostrar slide
function showSlide(index) {
    slides.forEach((slide, i) => {
        slide.classList.toggle('active', i === index);
    });
}

// Mostrar o primeiro slide ao carregar
showSlide(currentSlide);

// Eventos dos botões
prevBtn.addEventListener('click', () => {
    currentSlide = (currentSlide - 1 + slides.length) % slides.length;
    showSlide(currentSlide);
});

nextBtn.addEventListener('click', () => {
    currentSlide = (currentSlide + 1) % slides.length;
    showSlide(currentSlide);
});

// Interatividade de mensagens
const messageBtn = document.getElementById('messageBtn');
const messageBox = document.getElementById('messageBox');
const sendMessageBtn = document.getElementById('sendMessage');
const userMessageInput = document.getElementById('userMessage');
const messagesList = document.getElementById('messagesList');

messageBtn.addEventListener('click', () => {
    messageBox.classList.toggle('hidden');
});

sendMessageBtn.addEventListener('click', () => {
    const message = userMessageInput.value.trim();
    if (message) {
        const messageElement = document.createElement('p');
        messageElement.textContent = message;
        messagesList.appendChild(messageElement);
        userMessageInput.value = '';
        alert('Mensagem enviada! Obrigado por participar.');
        messageBox.classList.add('hidden');
    } else {
        alert('Por favor, escreva sua mensagem primeiro.');
    }
});
