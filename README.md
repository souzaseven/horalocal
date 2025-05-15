# ⏰ Hora Certa - Relógio Digital Inteligente

Um relógio digital moderno que exibe hora, data, localização e temperatura atual, com temas claro/escuro e design responsivo.
<!--
![Preview do Relógio](https://raw.githubusercontent.com/souzaseven/Site2/Desafios/icon%20eu.ico)
-->
## ✨ Funcionalidades

- **Relógio Digital Preciso**:
  - Exibe horas, minutos e segundos
  - Atualização em tempo real
  - Animação de pulsação suave

- **Informações Contextuais**:
  - Data completa por extenso (ex: "Sexta, 15 de Março de 2024")
  - Localização automática (cidade e país)
  - Temperatura atual em °C

- **Personalização**:
  - Alternância entre temas claro e escuro
  - Preferências salvas localmente
  - Design responsivo para todos dispositivos

- **Estatísticas**:
  - Contador de visitantes em tempo real

## 🛠️ Tecnologias Utilizadas

- **Frontend**:
  - HTML5 semântico
  - CSS3 com variáveis e animações
  - JavaScript (ES6+)

- **APIs Integradas**:
  - OpenWeatherMap (dados meteorológicos)
  - IP Geolocation (localização por IP)
  - Glitch (contador de visitas)

- **Bibliotecas**:
  - Google Analytics (métricas)
  - Google AdSense (monetização)

## 📂 Estrutura de Arquivos
hora-certa/ <br>
├── index.html # Página principal <br>
├── style.css # Estilos e temas <br>
└── script.js # Lógica do relógio e APIs <br>

## Obtenção de Localização

fetch('https://api.ipgeolocation.io/ipgeo?apiKey=SUA_CHAVE')
    .then(response => response.json())
    .then(data => {
        document.getElementById('location').textContent = `${data.city}, ${data.country_name}`;
    });

## Alternância de Temas

function toggleTheme() {
    const body = document.body;
    const isDark = body.classList.contains('dark-mode');
    
    body.classList.replace(isDark ? 'dark-mode' : 'light-mode', 
                         isDark ? 'light-mode' : 'dark-mode');
    localStorage.setItem('theme', isDark ? 'light' : 'dark');
}
