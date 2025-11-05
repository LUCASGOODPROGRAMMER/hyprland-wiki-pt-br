
````md
# 🧩 Sections
Sessões configuráveis no `hyprland.conf`.

---

## 🧩 Section: General

### 🔹 `border_size`
- Aceita valores do tipo **int** (inteiro).  
- Define o **tamanho das bordas** das janelas (*windows*).  
- Valor padrão: **1**.

---

### 🔹 `no_border_on_floating`
- Aceita valores **booleanos** (`true` / `false`).  
- Usado para **desativar as bordas** de janelas flutuantes (*floating windows*).  
- Valor padrão: **false**.

---

### 🔹 `gaps_in`
- Aceita valores **inteiros**.  
- Define o **espaçamento entre as janelas**.  
- Suporta o estilo CSS para gaps:

```text
top, right, bottom, left -> 5,10,15,20
````

---

### 🔹 `gaps_out`

* Aceita valores do tipo **int (integer)**.
* Define o **espaçamento entre as janelas e as bordas do monitor**.
* Também suporta o estilo CSS:

```text
top, right, bottom, left -> 5,10,15,20
```

* Valor padrão: **20**.

---

### 🔹 `float_gaps`

* Aceita valores **inteiros**.
* Define o **espaçamento entre janelas flutuantes** (*floating windows*) e as bordas do monitor.
* Também suporta o estilo CSS:

```text
top, right, bottom, left -> 12 5 3 1
```

* Se o valor for **-1**, o Hyprland usa o valor **padrão (0)**.

---

### 🔹 `gaps_workspaces`

* Aceita valores **inteiros**.
* Define o **espaçamento entre as áreas de trabalho** (*workspaces*).
* Valor padrão: **0**.

---

### 🔹 `col.inactive_border`

* Aceita valores de **gradiente**.
* Define a **cor das bordas** de janelas **inativas** ou **não focadas**.

---

### 🔹 `col.active_border`

* Aceita valores de **gradiente**.
* Define a **cor das bordas** de janelas **ativas** ou **focadas**.

---

### 🔹 `col.nogroup_border`

* Aceita valores de **gradiente**.
* Define a **cor das bordas** de janelas que **não podem ser adicionadas a um grupo**.

---

### 🔹 `layout`

* Aceita valores **string** (`str`).
* Define **qual layout será usado**.
* Valores possíveis:

  * `dwindle`
  * `master`

---

### 🧩 Section: General (continuação)

### 🔹 `no_focus_fallback`

* Aceita valores **booleanos** (`true` / `false`).
* Quando **true**, o Hyprland **não alterna automaticamente o foco** para outra janela ao tentar mover o foco em uma direção onde **nenhuma janela é encontrada**.
* Valor padrão: **false**.

---

### 🔹 `resize_on_border`

* Aceita valores **booleanos** (`true` / `false`).
* Ativa a **redimensionação de janelas clicando e arrastando** nas bordas ou nos gaps.
* Valor padrão: **false**.

---

### 🔹 `extend_border_grab_area`

* Aceita valores **inteiros**.
* Define o **tamanho da área extra em torno da borda** onde é possível clicar e arrastar para redimensionar.
* Só é usado quando `general:resize_on_border` está **ativado**.
* Valor padrão: **15**.

---

### 🔹 `hover_icon_on_border`

* Aceita valores **booleanos** (`true` / `false`).
* Exibe um **ícone de cursor** ao passar o mouse sobre as bordas da janela.
* Só é usado quando `general:resize_on_border` está **ativado**.
* Valor padrão: **true**.

---

### 🔹 `allow_tearing`

* Aceita valores **booleanos** (`true` / `false`).
* Habilita ou desabilita o **tearing** (efeito de corte de imagem durante movimentos rápidos de tela).
  Consulte a página [*Tearing*](https://wiki.hyprland.org/Configuring/Tearing/) da documentação para mais detalhes.
* Valor padrão: **false**.

---

### 🔹 `resize_corner`

* Aceita valores **inteiros**.
* Força as janelas flutuantes (*floating windows*) a usarem um **canto específico** durante o redimensionamento.
* Os valores possíveis vão de **1 a 4**, no sentido **horário a partir do canto superior esquerdo**:

```text
1 → canto superior esquerdo
2 → canto superior direito
3 → canto inferior direito
4 → canto inferior esquerdo
0 → desativado
```

* Valor padrão: **0**.


## Section: Snap (subcategoria de General)
### Sessão responsável por controlar como as janelas flutuantes se encaixam em realação a outras janelas ou ao monitor
```Exemplo de Snap:
General {
  ...
  Snap {...}
}
```
---

### Parâmetros Snap

#### enabled 

* tipo bool

* por padrão é igual a false

* tem a função de ativar ou desativar o encaixe de janelas flutuantes

---
#### window_gap

* tipo int

* por padrão seu valor é igual a 10.

* defini a distância miníma, em pixels, entre duas janelas antes que o snap aconteça (ou seja no momento em que a distância for igual a 10px as janelas vão grudar por conta do snap).

---

#### monitor_gap

* tipo int.

* por padrão seu valor é igual a 10.

* Defini a distância miníma entre o monitor e janela, para que o Snap aconteça.

---

#### border_overlap

* tipo bool.

* por padrão o seu valor é false.

* controla como as bordas das janelas se tocam quando o Slap é ativado.

* se o valor for false, as janelas vão parar antes de sobrepor, mantendo o gap definido.

* se o valor for true, elas vão se sobrepor leiramente - ficando apenas um borda de espaço entre elas
> *Útil para quem quer que as janelas pareçam **coladas** visualmente!*

---

#### respect_gaps

* tipo bool

* por padrão seu valor é false

* se for true o snapping respeita os gaps definidos no genereral:gaps_in

---

````Exemplo prático de configuração

  snap {
    enabled = true
    window_gap = 15
    monitor_gap = 10
    border_overlap = false
    respect_gaps = true
  }

````
---