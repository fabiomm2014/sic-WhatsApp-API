<h1 align="center">💬 SIC WhatsApp API 🇧🇷</h1>

<p align="center">
  <b>Simulador de cliente WhatsApp via API REST.</b><br>
  Envio de mensagens de texto, mídia e mensagens para grupos através de
  endpoints HTTP, com autenticação por QR Code em tempo real.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-12+-009C3B?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Express-4.17-FFDF00?style=for-the-badge&logo=express&logoColor=black" alt="Express">
  <img src="https://img.shields.io/badge/Socket.IO-2.3-002776?style=for-the-badge&logo=socketdotio&logoColor=white" alt="Socket.IO">
  <img src="https://img.shields.io/badge/WhatsApp-web.js-009C3B?style=for-the-badge&logo=whatsapp&logoColor=white" alt="whatsapp-web.js">
  <img src="https://img.shields.io/badge/Axios-HTTP-FFDF00?style=for-the-badge&logo=axios&logoColor=black" alt="Axios">
  <img src="https://img.shields.io/badge/Puppeteer-headless-002776?style=for-the-badge&logo=puppeteer&logoColor=white" alt="Puppeteer">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/-009C3B?style=flat-square&color=009C3B" height="6" width="120" alt="">
  <img src="https://img.shields.io/badge/-FFDF00?style=flat-square&color=FFDF00" height="6" width="120" alt="">
  <img src="https://img.shields.io/badge/-002776?style=flat-square&color=002776" height="6" width="120" alt="">
</p>

---

## 📑 Sumário

- [🔎 Visão geral](#-visão-geral)
- [✨ Funcionalidades](#-funcionalidades)
- [🛠️ Tecnologias](#️-tecnologias)
- [🚀 Como executar](#-como-executar)
- [🔌 Endpoints](#-endpoints)
- [🤖 Comandos do Bot](#-comandos-do-bot)
- [📄 Licença](#-licença)

---

## 🔎 Visão geral

Servidor **Node.js** que conecta ao WhatsApp via **whatsapp-web.js** (Puppeteer headless). A autenticação é feita por **QR Code** exibido em tempo real no navegador via **Socket.IO**. A sessão autenticada é salva em arquivo local (`whatsapp-session.json`) para reconexão automática. Suporta envio de texto, mídia e mensagens para grupos, além de funcionar como bot com respostas automáticas.

---

## ✨ Funcionalidades

| Módulo | Descrição |
| :----- | :-------- |
| 📱 **QR Code em tempo real** | Exibido no navegador via Socket.IO |
| 💬 **Envio de mensagens** | Texto para contatos individuais |
| 📎 **Envio de mídia** | Imagens/arquivos via URL externa |
| 👥 **Mensagens para grupos** | Por ID ou nome do grupo |
| 🧹 **Limpar chat** | Remover histórico de conversa |
| 🤖 **Bot automático** | Respostas a comandos (`!ping`, `!groups`) |
| 💾 **Persistência de sessão** | Reconexão automática sem novo QR |

---

## 🛠️ Tecnologias

| Camada | Tecnologia |
| :----- | :--------- |
| 💻 **Runtime** | Node.js v12+ |
| 🌐 **Framework web** | Express 4.17 |
| 📱 **WhatsApp** | whatsapp-web.js (Puppeteer/Chromium) |
| ⚡ **Tempo real** | Socket.IO 2.3 |
| 🔗 **HTTP client** | Axios 0.20 |
| ✅ **Validação** | express-validator 6.9 |
| 📷 **QR Code** | qrcode (data URL) |
| 🔄 **Dev** | nodemon |

---

## 🚀 Como executar

<details open>
<summary><b>▶️ Instalação e execução</b></summary>

```bash
npm install
npm start          # produção
npm run start:dev  # dev (nodemon)
```

Acesse `http://localhost:8000` para escanear o QR Code.

</details>

---

## 🔌 Endpoints

| Método | Rota | Descrição |
| :----- | :--- | :-------- |
| POST | `/send-message` | Enviar mensagem de texto (campos: `number`, `message`) |
| POST | `/send-media` | Enviar mídia via URL (campos: `number`, `caption`, `file`) |
| POST | `/send-group-message` | Enviar para grupo (campos: `id` ou `name`, `message`) |
| POST | `/clear-message` | Limpar histórico de chat (campo: `number`) |

---

## 🤖 Comandos do Bot

| Comando | Resposta |
| :------ | :------- |
| `!ping` | `pong` |
| `!groups` | Lista todos os grupos com ID e nome |
| `good morning` | `selamat pagi` |

---

## 📄 Licença

MIT

<p align="center">
  <img src="https://img.shields.io/badge/-009C3B?style=flat-square&color=009C3B" height="6" width="120" alt="">
  <img src="https://img.shields.io/badge/-FFDF00?style=flat-square&color=FFDF00" height="6" width="120" alt="">
  <img src="https://img.shields.io/badge/-002776?style=flat-square&color=002776" height="6" width="120" alt="">
</p>

<p align="center"><sub>Feito com 💚💛💙 — cores da bandeira do Brasil 🇧🇷</sub></p>
