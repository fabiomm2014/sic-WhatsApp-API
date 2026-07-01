# 💬 SIC WhatsApp API 🇧🇷

![Node.js](https://img.shields.io/badge/Node.js-12+-009C3B?style=flat&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-4.17-FFDF00?style=flat&logo=express&logoColor=black)
![Socket.IO](https://img.shields.io/badge/Socket.IO-2.3-002776?style=flat&logo=socketdotio&logoColor=white)

Simulador de cliente WhatsApp via API REST com envio de mensagens, midia e suporte a grupos.

## Visao geral

Servidor Node.js que conecta ao WhatsApp via **whatsapp-web.js** (Puppeteer headless). Autenticacao por QR Code exibido em tempo real no navegador via Socket.IO. Sessao salva em arquivo local para reconexao automatica. Funciona tambem como bot com comandos (`!ping`, `!groups`).

## Endpoints

| Metodo | Rota | Descricao |
|--------|------|-----------|
| POST | `/send-message` | Enviar mensagem de texto |
| POST | `/send-media` | Enviar midia (via URL) |
| POST | `/send-group-message` | Enviar para grupo (ID ou nome) |
| POST | `/clear-message` | Limpar historico de chat |

## Tecnologias

- **Node.js v12+** / **Express 4.17**
- **whatsapp-web.js** (Puppeteer/Chromium)
- **Socket.IO 2.3** (QR code em tempo real)
- **Axios** (download de midia)
- **express-validator** (validacao de requisicoes)
- **nodemon** (dev)

## Como executar

```bash
npm install
npm start          # ou npm run start:dev (nodemon)
```

Acesse `http://localhost:8000` para escanear o QR Code.

## Licenca

MIT

---
*Feito com 💚💛💙 — cores da bandeira do Brasil 🇧🇷*
