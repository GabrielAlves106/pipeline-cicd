# Pipeline CI/CD

Um projeto demonstrando configuração e implementação de uma pipeline de Integração Contínua/Entrega Contínua (CI/CD).

## 📋 Descrição

Este projeto é um exemplo prático de como estruturar e executar uma pipeline CI/CD utilizando Python. A pipeline automatiza testes e validações de código através de workflows configurados no GitHub Actions.

## 🚀 Funcionalidades

- Aplicação Python modular
- Suite de testes automatizados
- Pipeline CI/CD integrada com GitHub Actions
- Validação automática de código
- Testes executados a cada push/pull request

## 🛠️ Tecnologias

- **Linguagem**: Python 3.x
- **CI/CD**: GitHub Actions
- **Testes**: pytest (ou framework de testes Python)

## 📁 Estrutura do Projeto

```
pipeline-cicd/
├── .github/
│   └── workflows/          # Configurações de GitHub Actions
├── app.py                  # Arquivo principal da aplicação
├── test_app.py            # Testes unitários
├── requirements.txt       # Dependências do projeto
├── .gitignore            # Arquivos ignorados pelo Git
└── README.md             # Este arquivo
```

## 📦 Dependências

As dependências do projeto estão listadas em `requirements.txt`:

```
pytest
```

Para instalar as dependências, execute:

```bash
pip install -r requirements.txt
```

## 💻 Como Usar

### Instalação

1. Clone o repositório:
```bash
git clone https://github.com/GabrielAlves106/pipeline-cicd.git
cd pipeline-cicd
```

2. Crie um ambiente virtual (recomendado):
```bash
python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate
```

3. Instale as dependências:
```bash
pip install -r requirements.txt
```

### Executar a Aplicação

```bash
python app.py
```

### Executar os Testes

```bash
pytest test_app.py
```

Ou para testes com saída mais verbosa:

```bash
pytest test_app.py -v
```

## 🔄 Pipeline CI/CD

A pipeline é automaticamente acionada quando você:

- Faz um **push** para a branch `main`
- Abre ou atualiza um **pull request**

### Etapas da Pipeline

1. **Checkout** - Faz clone do código
2. **Setup Python** - Configura o ambiente Python
3. **Install Dependencies** - Instala dependências do projeto
4. **Run Tests** - Executa a suite de testes
5. **Validação** - Verifica se os testes passaram

Você pode visualizar o status da pipeline em: **Actions** → Clique no workflow desejado

## 📝 Contribuição

Para contribuir com o projeto:

1. Crie uma branch para sua feature (`git checkout -b feature/MinhaFeature`)
2. Commit suas mudanças (`git commit -m 'Add MinhaFeature'`)
3. Faça push para a branch (`git push origin feature/MinhaFeature`)
4. Abra um Pull Request

Certifique-se de que todos os testes passam antes de enviar seu PR!

## ⚠️ Testes

Todo código deve ter testes associados. Para adicionar novos testes:

1. Crie funções de teste em `test_app.py` (ou em novo arquivo seguindo o padrão `test_*.py`)
2. Use nomes descritivos para as funções de teste
3. Garanta que os testes passam localmente antes de fazer push

```python
def test_exemplo():
    assert resultado_esperado == resultado_obtido
```

## 🐛 Troubleshooting

### Testes falhando localmente
- Verifique se todas as dependências foram instaladas: `pip install -r requirements.txt`
- Certifique-se de estar no ambiente virtual correto

### Pipeline falhando no GitHub Actions
- Verifique os logs na aba **Actions** do repositório
- Rode os testes localmente para reproduzir o erro
- Verifique o arquivo de workflow em `.github/workflows/`

## 📞 Suporte

Para dúvidas ou problemas, abra uma **Issue** no repositório.

## 📄 Licença

Este projeto está disponível como código aberto. Consulte a licença do repositório para mais detalhes.

---

**Criado por**: [GabrielAlves106](https://github.com/GabrielAlves106)  
**Última atualização**: 2026-03-12