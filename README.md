# 🌸 Lu Cerimonialista — App de Check-in para Eventos

Aplicativo web para **check-in de convidados** com QR Code, lista de presença,
controle de mesas e sincronismo em nuvem entre vários celulares.

## ✨ O que faz

- 📷 **Portaria**: lê QR Code pela câmera ou de imagem, confirma presença
- 📋 **Lista de convidados**: importar CSV, buscar, filtrar, editar
- 🪑 **Controle de mesas** com toast de mesa completa
- ☁️ **Nuvem automática**: todos os celulares sincronizam sozinhos (MQTT)
- 📴 **Funciona off-line**: Backup/Restore em arquivo
- 🔤 **Corrige acentos** automaticamente (dicionário de nomes brasileiros)
- 📲 **PWA**: instalável no iPhone e Android, sem zoom, só rolagem
- 🖨️ Imprime QRs, exporta CSV, convite via WhatsApp

## 📁 Estrutura

| Arquivo | O quê |
|---|---|
| `index.html` | O app inteiro (arquivo único, funciona off-line) |
| `vercel.json` | Config da Vercel |
| `manifest.webmanifest` + `icon-*.png` | PWA / ícone de instalar |
| `apple-touch-icon.png` + `splash-*.jpg` | iPhone (ícone + telas de abertura) |

## 🚀 Publicar

1. Suba estes arquivos para um repositório no **GitHub**
2. Na **Vercel**: *Add New → Project → Import* o repositório
3. Deploy automático — cada `push` atualiza o site

> Guia passo a passo (em português): veja `COMO-PUBLICAR-NO-GITHUB.md`

## 🛠️ Notas técnicas

- Arquivo único, sem build: HTML + CSS + JS inline (libs: QRCode, jsQR, MQTT)
- Dados locais em `localStorage`, nuvem via MQTT (zero configuração)
- Português (pt-BR)
