# 🤖 Reconhecimento Facial

Script de reconhecimento facial em tempo real utilizando câmeras, capaz de identificar pessoas ou objetos previamente cadastrados e emitir alerta visual para entidades não reconhecidas — compatível com qualquer câmera ou dispositivo.

## 🎥 Demonstração

> 📺 **Veja o projeto em funcionamento:** [Assistir no YouTube](https://www.youtube.com/watch?v=dd-mQ8Uuh4k)

---

## ✨ Funcionalidades

- 📸 **Reconhecimento em tempo real** via câmera (webcam, câmera IP ou celular)
- 🗂️ **Cadastro simples** — basta adicionar uma foto do rosto na pasta do sistema
- ✅ **Identificação** de pessoas e objetos previamente cadastrados com exibição do nome
- ⚠️ **Alerta de desconhecido** — exibe um quadrado delimitador e a mensagem "Desconhecido" para rostos não reconhecidos
- ⚡ **Processamento paralelo** com threads para melhor performance em tempo real
- 🌐 **Compatível** com qualquer dispositivo que forneça feed de câmera

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Descrição |
|------------|-----------|
| ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) | Linguagem principal do projeto |
| ![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white) | Captura de vídeo e processamento de imagens |
| `face_recognition` | Detecção e comparação de rostos com alta precisão |
| `dlib` | Base de modelos de aprendizado de máquina para detecção facial |
| `NumPy` | Manipulação eficiente de arrays e dados de imagem |
| `threading` | Processamento paralelo para performance em tempo real |

---

## 📁 Estrutura do Projeto

```
reconhecimento-facial/
├── faces/              # Pasta onde as imagens cadastradas são adicionadas
│   ├── pessoa1.jpg
│   ├── pessoa2.png
│   └── ...
├── main.py             # Script principal de reconhecimento facial
├── .gitignore
└── README.md           # Documentação do projeto
```

---

## ⚙️ Como Funciona

1. **Cadastro:** adicione qualquer imagem de rosto na pasta `faces/` — o nome do arquivo será usado como identificador
2. **Execução:** ao rodar o script, o sistema carrega todas as imagens da pasta e extrai os encodings faciais
3. **Reconhecimento:** o feed da câmera é processado em tempo real frame a frame
4. **Resultado:**
   - Rosto **reconhecido** → quadrado colorido com o **nome da pessoa**
   - Rosto **desconhecido** → quadrado delimitador com a mensagem **"Desconhecido"**

---

## 🚀 Como Executar

### Pré-requisitos

- Python 3.8+
- CMake instalado (necessário para compilar o `dlib`)

### Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/mor3sco/reconhecimento-facial.git
   cd reconhecimento-facial
   ```

2. Instale as dependências:
   ```bash
   pip install opencv-python face_recognition numpy dlib
   ```

3. Adicione as imagens das pessoas na pasta `faces/`:
   ```
   faces/
   ├── Evandro.jpg
   └── outro_nome.png
   ```

4. Execute o script:
   ```bash
   python main.py
   ```

---

## 💡 Aprendizados

Este projeto foi desenvolvido para explorar **visão computacional** e conceitos de **segurança com IA**:

- Uso de **modelos pré-treinados** de detecção facial com `dlib` e `face_recognition`
- Captura e processamento de **vídeo em tempo real** com OpenCV
- Implementação de **multithreading** para evitar travamentos durante o processamento
- Manipulação de **arrays de imagem** com NumPy
- Desenvolvimento de um sistema de cadastro **sem banco de dados**, baseado em arquivos

---

<p align="center">
  Feito por <a href="https://github.com/mor3sco"><strong>Evandro Moresco</strong></a>
</p>
