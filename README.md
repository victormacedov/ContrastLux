# ContrastLux

**ContrastLux** é uma ferramenta interativa para ajuste de **brilho e contraste** de imagens, com visualização em **tempo real** e preservação de detalhes através do **CLAHE** (Contrast Limited Adaptive Histogram Equalization). Ideal para fotógrafos, designers e qualquer pessoa que queira melhorar suas imagens de forma rápida e intuitiva.

---

## 🖼️ Funcionalidades

* **Upload de imagens**: suporta JPEG, PNG, BMP e TIFF.
* **Controle de brilho e contraste**: sliders interativos para ajustes em tempo real.
* **Visualização antes/depois**: compara a imagem original com a imagem ajustada lado a lado.
* **CLAHE opcional**: preserva detalhes em áreas escuras e claras, podendo ser ativado/desativado com a tecla `C`.
* **Reset rápido**: tecla `R` para restaurar brilho e contraste aos valores padrão.
* **Salvar imagem editada**: exporta a imagem em JPEG, PNG, BMP ou TIFF.
* **Zoom**: aumente ou diminua o zoom da imagem com as teclas `+` e `-`, visualizando o nível de zoom na interface.

---

## ⚡ Requisitos

* Python 3.8+
* Bibliotecas:

  * `opencv-python`
  * `numpy`
  * `tqdm`
  * `tkinter` (normalmente incluído no Python padrão)

---

## 💻 Instalação

1. Clone este repositório:

```bash
git clone https://github.com/victormacedov/ContrastLux.git
cd ContrastLux
```

2. Instale as dependências:

```bash
pip install -r requirements.txt
```

*(Tkinter geralmente já vem com Python; caso não tenha, instale conforme seu SO.)*

---

## 🚀 Uso

Execute o script principal:

```bash
python main.ipynb
```

1. Uma janela será aberta para selecionar a imagem.
2. Ajuste o **brilho** e o **contraste** com os sliders.
3. Pressione **C** para ativar/desativar CLAHE e observar a preservação de detalhes.
4. Pressione **R** para resetar brilho e contraste aos valores padrão.
5. Use `+` ou `-` para ajustar o zoom da imagem.
6. Pressione **Esc** para fechar a janela.
7. Escolha onde salvar a imagem editada quando solicitado.

---

## 🛠️ Como funciona

* **Brilho**: soma ou subtrai um valor constante em cada pixel, limitado a \[0, 255].
* **Contraste**: aplica a fórmula `novo_pixel = fator_contraste * (pixel_original - 128) + 128`.
* **CLAHE**: equaliza o histograma de forma adaptativa em pequenas regiões da imagem, evitando perda de detalhes em sombras ou áreas claras.

---

## 🔑 Atalhos de Teclado

| Tecla  | Função                                              |
|--------|-----------------------------------------------------|
| `C`    | Alternar CLAHE ON/OFF                               |
| `R`    | Resetar brilho e contraste para valores padrão      |
| `+`/`-`| Aumentar ou diminuir o zoom                         |
| `Esc`  | Fechar aplicação                                    |

---

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.