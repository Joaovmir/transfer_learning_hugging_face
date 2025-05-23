# Transfer Learning Hugging Face ✨✍️

[![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)

Aplicativo de IA que utiliza **transferência de aprendizado** com modelos pré-treinados da Hugging Face para atribuir notas automáticas a redações em português, incentivando a prática e o aprimoramento dos estudantes.

---

## ✨ Visão Geral

O **transfer_learning_hugging_face** resolve o problema de limitação de correção manual de redações em cursos preparatórios, permitindo que os alunos pratiquem à vontade e recebam feedback imediato. A solução utiliza modelos zero-shot para classificação textual, sem a necessidade de treinar do zero, facilitando a aplicação para diferentes tarefas de avaliação.

---

## 📚 Tecnologias Utilizadas

- [Python 3.8+](https://www.python.org/)
- [Transformers (Hugging Face)](https://huggingface.co/docs/transformers/index)
- [PyTorch](https://pytorch.org/)

---

## ⚡ Instalação e Uso

### 1. Clone o repositório

```bash
git clone https://github.com/Joaovmir/transfer_learning_hugging_face.git
cd transfer_learning_hugging_face
````

### 2. Instale as dependências

No Google Colab, basta executar as primeiras células do notebook.

Para uso local, execute:

```bash
pip install transformers torch
```

### 3. Execute o notebook

Abra e execute o arquivo `Projeto_Transferência_de_aprendizado_com_Hugging_Face.ipynb` em seu ambiente preferido (Jupyter, VS Code ou Colab).

---

## 💡 Exemplo de Uso

O projeto utiliza o modelo zero-shot [`Mel-Iza0/zero-shot`](https://huggingface.co/Mel-Iza0/zero-shot), que permite classificar textos em português conforme critérios personalizados.

Exemplo de aplicação:

```python
from transformers import pipeline

classifier = pipeline("zero-shot-classification", model="Mel-Iza0/zero-shot")
texto_redacao = "A redação deve ser clara, objetiva e bem estruturada."
labels = ["excelente", "regular", "precisa melhorar"]
resultado = classifier(texto_redacao, candidate_labels=labels)
print(resultado)
```

**Saída esperada:**
O modelo atribui uma nota/label de acordo com o conteúdo da redação.

---

## 📁 Estrutura do Projeto

```
transfer_learning_hugging_face/
├── Projeto_Transferência_de_aprendizado_com_Hugging_Face.ipynb
├── README.md
  └── dados
```

> **Obs:** O projeto pode ser facilmente adaptado para outras tarefas de classificação de textos em português usando modelos Hugging Face.
