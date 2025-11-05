````md
# 🧩 Hyprland — Tipos de Variáveis (Variable Types)

---

## 🧠 O que são tipos de variáveis?

No Hyprland, cada parâmetro de configuração possui um **tipo de valor específico** — por exemplo, número, texto, cor ou vetor.  
Saber identificar o tipo correto é essencial para evitar erros no arquivo `hyprland.conf`.

---

## 🔢 Tipos de variáveis disponíveis

### e.g. *(exempli gratia / por exemplo)*

| Tipo | Descrição | Exemplo |
|------|------------|---------|
| **int** | Números inteiros. | `5`, `-2`, `100` |
| **bool** | Valores booleanos *(on/off, true/false, 0/1, yes/no)*. | `true`, `false` |
| **float** | Números com casas decimais. | `0.5`, `2.75` |
| **color** | Define uma cor (veja abaixo as opções disponíveis). | `rgba(b3ff1aee)` |
| **vec2** | Vetor com 2 valores *float* separados por espaço. | `0 0`, `1.2 3.4` |
| **MOD** | Teclas modificadoras *(modmask)*. | `SUPER`, `SUPER + SHIFT`, `CTRL_SHIFT` |
| **str** | Texto (string). | `"example"`, `dwindle` |
| **gradient** | Gradiente de cores *(sintaxe: `color color ... [angle]deg`)*. | `rgba(33ccffee) rgba(00ff99ee) 45deg` |
| **font_weight** | Peso da fonte, numérico (`100–1000`) ou textual. | `bold`, `semilight`, `300` |

---

## 🎨 Definindo cores

O Hyprland aceita **três formatos principais de cor**:

| Formato | Exemplo | Observações |
|----------|----------|-------------|
| **rgba()** | `rgba(b3ff1aee)` ou `rgba(179,255,26,0.933)` | *Os valores decimais não devem conter espaços.* |
| **rgb()** | `rgb(b3ff1a)` ou `rgb(179,255,26)` | Sem canal alfa. |
| **legacy (ARGB)** | `0xeeb3ff1a` | Formato antigo, ordem **ARGB**. |

---

## ⌨️ Lista de teclas modificadoras *(modmask)*

Essas teclas são usadas em combinações de atalhos no Hyprland:

```text
SHIFT, CAPS, CTRL / CONTROL, ALT, MOD2, MOD3, SUPER / WIN / LOGO / MOD4, MOD5
````

---

## 💡 Dica

Para entender melhor como cada tipo é aplicado em seções específicas (como `general`, `decoration`, `animations`, etc.), consulte a [documentação oficial de Variáveis](https://wiki.hyprland.org/Configuring/Variables/#variable-types).

```
```
