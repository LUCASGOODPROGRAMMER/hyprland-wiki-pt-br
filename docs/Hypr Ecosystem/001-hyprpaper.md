# Manual de Configuração — Hyprpaper

## 📘 Introdução
O **Hyprpaper** é o gerenciador de papéis de parede (wallpaper manager) utilizado em ambientes com **Hyprland**. Ele é leve, rápido e totalmente configurável via arquivo de texto.

---

## ⚙️ Instalação

### Arch Linux (ou derivados)
Para instalar o Hyprpaper no Arch Linux ou sistemas baseados nele:

```bash
sudo pacman -S hyprpaper
```

Caso esteja usando o AUR:

```bash
yay -S hyprpaper
```

### Debian / Ubuntu
Em sistemas baseados em Debian:

```bash
sudo apt install hyprpaper
```

Se o pacote não estiver disponível, você pode compilá-lo manualmente pelo repositório oficial do Hyprland.

---

## 📂 Localização e Criação do Arquivo de Configuração

O arquivo de configuração padrão do **Hyprpaper** fica em:

```
~/.config/hypr/hyprpaper.conf
```

Se não existir, crie-o manualmente com:

```bash
mkdir -p ~/.config/hypr
touch ~/.config/hypr/hyprpaper.conf
```

---

## 🧾 Estrutura do Arquivo de Configuração

Um exemplo simples de configuração é o seguinte:

```bash
preload = /usr/share/backgrounds/wallpaper1.png
preload = /usr/share/backgrounds/wallpaper2.png

wallpaper = eDP-1,/usr/share/backgrounds/wallpaper1.png
wallpaper = HDMI-A-1,/usr/share/backgrounds/wallpaper2.png

# Modo de recarregar automaticamente o wallpaper (opcional)
# wallpaper_mode = center | stretch | fill | fit
```

---

## 💡 Explicando as Diretivas

| Diretiva | Função |
|-----------|---------|
| `preload` | Carrega previamente a imagem para evitar atrasos ao aplicar. |
| `wallpaper` | Define qual monitor recebe qual imagem. |
| `wallpaper_mode` | Define como a imagem é ajustada (center, fill, stretch, etc.). |

---

## 🖥️ Aplicando e Testando o Hyprpaper

Para iniciar o Hyprpaper manualmente:

```bash
hyprpaper &
```

Caso queira que ele inicie automaticamente junto com o Hyprland, adicione ao arquivo de configuração do **Hyprland** (`~/.config/hypr/hyprland.conf`):

```bash
exec-once = hyprpaper &
```

---

## 🪄 Dicas e Soluções

- Se o wallpaper não aparecer, verifique se o caminho do arquivo está correto e acessível.
- Use caminhos absolutos (ex: `/home/usuario/Imagens/fundo.png`).
- Se estiver usando múltiplos monitores, confirme o nome exato de cada um com:
  
  ```bash
  hyprctl monitors
  ```

---

## 🧹 Dica Extra — Reload Rápido

Você pode atualizar a imagem do wallpaper sem reiniciar o Hyprland:

```bash
killall hyprpaper && hyprpaper &
```

---

## 🧾 Exemplo Completo

```bash
# Hyprpaper configuration file

# Pre-carrega wallpapers
preload = ~/Imagens/wallpapers/montanha.png
preload = ~/Imagens/wallpapers/praia.png

# alinha os wallpapers no(s) monitor(es)
wallpaper = eDP-1,~/Imagens/wallpapers/montanha.png
wallpaper = HDMI-A-1,~/Imagens/wallpapers/praia.png

# modo opcional para wallpaper
wallpaper_mode = fill
```

---

