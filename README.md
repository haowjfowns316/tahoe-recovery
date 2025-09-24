# A workflow file that generates macOS Tahoe recovery image

### Full installer downloaded straight from Apple and then recover image is extracted

---

## 🇧🇷 Explicação em Português

### Como funciona este projeto?

Este projeto **NÃO precisa ser executado no seu computador**. Ele funciona automaticamente no GitHub usando macOS virtual.

**Resumo simples:**
1. Você faz um "fork" (cópia) deste repositório no seu GitHub
2. Executa uma "Action" (processo automático) que roda em um macOS virtual do GitHub
3. O sistema baixa automaticamente o instalador do macOS Tahoe direto da Apple
4. Extrai os arquivos de recuperação necessários
5. Você baixa o arquivo `com.apple.recovery.boot.zip` gerado

### Posso usar no Windows?

**SIM!** Você pode usar a imagem de recuperação gerada no Windows para instalar macOS.

**O que precisa de macOS:** Apenas a GERAÇÃO da imagem (que acontece automaticamente no GitHub)
**O que funciona no Windows:** Usar a imagem gerada para instalar macOS no seu PC

### Passo a passo completo:

1. **Fork este repositório** (botão "Fork" no canto superior direito)
2. **No seu fork, vá na aba "Actions"**
3. **Escolha um workflow:**
   - `Tahoe Beta 1 Recovery Image` - Para a primeira beta
   - `Tahoe Beta (latest) Recovery Image` - Para a beta mais recente  
   - `Tahoe Public Recovery Image` - Para a versão pública (quando disponível)
4. **Clique em "Run workflow"**
5. **Aguarde** o processo terminar (pode demorar 30-60 minutos)
6. **Baixe o arquivo** `com.apple.recovery.boot.zip` dos artifacts
7. **Descompacte** para obter `com.apple.recovery.boot`
8. **Continue com o guia do OpenCore:**
   - Windows: https://dortania.github.io/OpenCore-Install-Guide/installer-guide/windows-install.html
   - Linux: https://dortania.github.io/OpenCore-Install-Guide/installer-guide/linux-install.html
   - **Pule a parte de "Downloading macOS"** pois este repositório já fez isso para você

### Perguntas Frequentes (FAQ):

**P: Preciso ter macOS para usar isso?**
R: NÃO! Você só precisa de uma conta no GitHub. O macOS é usado automaticamente nos servidores do GitHub.

**P: Funciona no Windows?**
R: SIM! A imagem gerada pode ser usada no Windows para instalar macOS.

**P: É gratuito?**
R: SIM! O GitHub Actions é gratuito para repositórios públicos.

**P: É legal?**
R: SIM! Este projeto apenas automatiza o download oficial da Apple, não distribui software pirata.

---

## 🚨Updates🚨

I renamed `Generate macOS Tahoe Recovery Image` workflow to `Tahoe Beta 1 Recovery Image`, this will always generate the recovery image for the first beta of Tahoe.

But if you are looking for the latest beta recovery image run `Tahoe Beta (latest) Recovery Image`

For public release `Tahoe Public Recovery Image`

## 🔧 Troubleshooting

**Q: Workflow failed with "Could not find Install macOS app"**
A: This usually means the download link is outdated. Please open an issue.

**Q: Artifact download gives me an empty or corrupted file**
A: Wait for the workflow to completely finish before downloading. Check the workflow logs for errors.

**Q: OpenCore guide says I need a different recovery image**
A: Make sure you're using the correct workflow - Beta versions may not be compatible with stable OpenCore releases.

**Q: Can I run multiple workflows at the same time?**
A: Yes, but GitHub limits concurrent jobs. It's better to run them one at a time.

# Why you may need this ?

Without the recovery image, you need to be on macOS to install Tahoe. Since there's no stable release yet, no official recovery images are available either.
This repo will fetch the full beta installer and zip what you need to have in order to install Tahoe from recovery.

# How to use this? 

## Requirements
- **GitHub account** (free)
- **No macOS required** - This runs automatically on GitHub's macOS servers
- **Works on Windows, Linux, and macOS** for the final installation

## Step-by-step instructions:

1. **Fork this repository** (click "Fork" button in the top-right corner)
2. **Go to the "Actions" tab** in your forked repository
3. **Choose and run a workflow:**
   - `Tahoe Beta 1 Recovery Image` - First beta release
   - `Tahoe Beta (latest) Recovery Image` - Latest beta version
   - `Tahoe Public Recovery Image` - Public release version
4. **Click "Run workflow"** and wait for completion (30-60 minutes)
5. **Download** the `com.apple.recovery.boot.zip` artifact from the completed workflow
6. **Extract** the ZIP file to get `com.apple.recovery.boot` folder
7. **Continue with OpenCore installation guide:**
   - **Windows:** https://dortania.github.io/OpenCore-Install-Guide/installer-guide/windows-install.html
   - **Linux:** https://dortania.github.io/OpenCore-Install-Guide/installer-guide/linux-install.html
   
   ⚠️ **Skip the "Downloading macOS" section** - this repository already did that for you!

## 💡 Important Notes:
- The **generation** process requires macOS (handled automatically by GitHub Actions)
- The **generated recovery image** can be used on **Windows, Linux, or macOS**
- This is completely **free** using GitHub's infrastructure
- **No software piracy** - downloads official Apple installers

## ⚠️ Legal Notice & Disclaimer

## This project does not distribute, modify, or host any Apple software.

- I do not own or claim ownership of any Apple software referenced or downloaded.

- This project is for educational and personal use only.

- No warranty or guarantee is provided—use at your own risk.

- Apple, macOS, and related marks are trademarks of Apple Inc., registered in the U.S. and other countries.
