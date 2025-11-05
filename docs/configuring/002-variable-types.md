````md
# 🧩 Tipos de Variáveis — Hyprland

---

## 🧠 Introdução

Cada parâmetro dentro do `hyprland.conf` possui um **tipo de valor** que define como ele deve ser escrito e interpretado.  
Compreender esses tipos é essencial para evitar erros de sintaxe e aplicar corretamente as opções.

---

## 🔢 Tipos disponíveis

### 💬 *e.g.* (*exempli gratia / por exemplo*)

---

### 🔹 `int`
- **Descrição:** números inteiros.  
- **Exemplo:** `5`, `-2`, `100`

---

### 🔹 `bool`
- **Descrição:** valores booleanos.  
- **Aceita:** `on` / `off`, `true` / `false`, `0` / `1`, `yes` / `no`  
- **Exemplo:** `true`

---

### 🔹 `float`
- **Descrição:** números com casas decimais.  
- **Exemplo:** `0.5`, `2.75`

---

### 🔹 `color`
- **Descrição:** define uma cor (veja abaixo os formatos aceitos).  
- **Exemplo:** `rgba(b3ff1aee)`

---

### 🔹 `vec2`
- **Descrição:** vetor com 2 valores *float*, separados por espaço.  
- **Exemplo:**  
  ```conf
  vec2 = 0 0
  vec2 = 1.2 3.4
````

---

### 🔹 `MOD`

* **Descrição:** conjunto de teclas modificadoras (*modmask*).
* **Exemplo:** `SUPER`, `SUPER + SHIFT`, `CTRL_SHIFT`

---

### 🔹 `str`

* **Descrição:** sequência de caracteres (*string*).
* **Exemplo:** `"example"`, `dwindle`

---

### 🔹 `gradient`

* **Descrição:** gradiente de cores.
* **Sintaxe:**

  ```conf
  color1 color2 ... [ângulo]deg
  ```
* **Exemplo:**

  ```conf
  rgba(33ccffee) rgba(00ff99ee) 45deg
  ```

---

### 🔹 `font_weight`

* **Descrição:** define o peso da fonte.
* **Aceita:** valores de `100` a `1000`, ou nomes como:
  `thin`, `light`, `normal`, `medium`, `bold`, `semibold`, `heavy`
* **Exemplo:** `bold`, `300`

---

## 🎨 Formatos de cor aceitos

Existem três maneiras principais de definir cores no Hyprland:

---

### 🔸 `rgba()`

```conf
rgba(b3ff1aee)
rgba(179,255,26,0.933)
```

> 💡 *Os valores decimais não devem conter espaços.*

---

### 🔸 `rgb()`

```conf
rgb(b3ff1a)
rgb(179,255,26)
```

> *Sem canal alfa.*

---

### 🔸 `legacy (ARGB)`

```conf
0xeeb3ff1a
```

> *Formato antigo, na ordem **ARGB**.*

---

## ⌨️ Teclas Modificadoras (*modmask*)

Essas teclas podem ser usadas em **atalhos e binds**:

```text
SHIFT, CAPS, CTRL / CONTROL, ALT, MOD2, MOD3, SUPER / WIN / LOGO / MOD4, MOD5
```

---

## 💡 Dica

Consulte a seção [Variables](https://wiki.hyprland.org/Configuring/Variables/#variable-types) na Wiki oficial do Hyprland para entender como cada tipo é usado dentro das seções (`general`, `decoration`, `animations`, etc.).

```
```
