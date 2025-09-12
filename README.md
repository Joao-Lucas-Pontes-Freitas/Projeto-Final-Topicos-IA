z# Variational Autoencoder for Cartoon Dataset

## Dataset
- 10k imagens de rostos de desenhos animados.
- Baixe em: [https://google.github.io/cartoonset/download.html](https://google.github.io/cartoonset/download.html)
- Após baixar, extraia as imagens para uma pasta `cartoonset10k/`.

## Ambiente
- Python 3.11.7
- Dependências listadas em `pyproject.toml`

## Instruções de uso

### 1. Clonar repositório
```bash
git clone https://github.com/Joao-Lucas-Pontes-Freitas/Projeto-Final-Topicos-IA
cd Projeto-Final-Topicos-IA
```

### 2. Criar e ativar ambiente virtual

#### Windows (PowerShell)

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
uv venv --python 3.11.7
```

#### Linux / macOS

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
uv venv --python 3.11.7
```

### 3. Instalar dependências

```bash
uv sync
```

### 4. Organizar dados

Coloque a pasta `cartoonset10k/` dentro do projeto:

```
VAE_Cartoon/
 ├─ cartoonset10k/
 │   ├─ img000000.png
 │   ├─ img000001.png
 │   └─ ...
 ├─ VAE_Cartoon_TensorFlow.ipynb
 └─ requirements.txt
```

### 5. Treinar o modelo

* No notebook, ajuste `DATA_DIR` para o caminho correto do `cartoonset10k`.
* Execute o notebook.
* Pesos são salvos em `tf_vae/cartoon/training_weights/`.
* Imagens geradas são salvas em `tf_vae/cartoon/images/`.

### 6. Resultados

* **Pesos do encoder/decoder** por época.
* **Mosaicos de amostras** por época.
* **t-SNE** do espaço latente.
* **Reconstruções** e **amostras** do gerador.

## Referências
* Link para o artigo de referência: [learnopencv](https://learnopencv.com/variational-autoencoder-in-tensorflow)
* Link para o github de referência: [github](https://github.com/spmallick/learnopencv/tree/master/Variational-Autoencoder-TensorFlow)
---