# 📘 Como publicar o app no GitHub (passo a passo)

> Para que serve? Guardar seu app no **GitHub** e ligar na **Vercel**.
> Depois disso, cada atualização que você subir aparece no site sozinha. ✨

---

## 🅰️ OPÇÃO A — Pelo site (mais fácil, sem instalar nada)

### 1. Criar conta no GitHub
1. Abra: **https://github.com**
2. Clique em **Sign up** e crie sua conta (grátis)

### 2. Criar o repositório (a "pasta" do app)
1. Clique no **＋** (canto superior direito) → **New repository**
2. **Repository name**: `lu-cerimonialista`
3. Deixe **Public** marcado
4. Marque ✅ **Add a README file**
5. Clique em **Create repository**

### 3. Subir os arquivos do app
1. Dentro do repositório, clique em **Add file** → **Upload files**
2. Arraste **todos os arquivos** da pasta `github-lu-cerimonialista`:
   - `index.html`, `vercel.json`, `manifest.webmanifest`
   - `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`
   - os 4 `splash-*.jpg`, `README.md`, `.gitignore`
3. Clique em **Commit changes** (botão verde)

✅ Pronto! Seu app está no GitHub.

---

## 🅱️ OPÇÃO B — Com git no computador (para quem já usa terminal)

```bash
# 1. Entre na pasta do app
cd github-lu-cerimonialista

# 2. Inicie o repositório e faça o primeiro commit
git init
git add .
git commit -m "App Lu Cerimonialista"

# 3. Crie o repositório no GitHub (site) e ligue ele aqui:
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/lu-cerimonialista.git
git push -u origin main
```

> Troque `SEU-USUARIO` pelo seu nome de usuário do GitHub.

### Atualizar depois (quando mudar algo no app)

```bash
git add .
git commit -m "Atualização"
git push
```

---

## 🔗 Ligar a Vercel no GitHub (deploy automático)

Faça **uma vez só**:

1. Abra: **https://vercel.com** → entre com a conta (pode entrar com o GitHub)
2. Clique em **Add New…** → **Project**
3. Em *Import Git Repository*, escolha **`lu-cerimonialista`** → **Import**
4. Não mude nada (o `vercel.json` já está certo) → clique em **Deploy**
5. Espere ~1 minuto → você ganha o link do app 🎉

**A partir daí:** toda vez que você subir arquivo novo no GitHub
(pela Opção A ou B), a Vercel **atualiza o site sozinha**. Sem ZIP, sem reenviar nada.

---

## ❓ Dúvidas comuns

| Dúvida | Resposta |
|---|---|
| Preciso pagar? | Não. GitHub e Vercel têm plano grátis que basta. |
| Repositório Public ou Private? | Tanto faz — a Vercel publica dos dois. |
| Errei um arquivo, e agora? | Suba de novo por cima (Opção A) ou faça novo `push` (Opção B). |
| Onde fica o link do app? | No painel da Vercel → seu projeto → *Visit*. |
| Preciso do ZIP ainda? | Não, depois que ligar o GitHub. Guarde o ZIP só como backup. |

---

*Feito com 🌸 para a Lu Cerimonialista*
