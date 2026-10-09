# Explorando Práticas de Teste

Neste exercício, vamos explorar práticas de teste em sistemas reais utilizando a ferramenta [TestMiner](https://andrehora.github.io/testminer).

O TestMiner permite visualizar e analisar testes de software em repositórios do GitHub, fornecendo dados sobre como os projetos organizam seus testes, como eles evoluem entre versões e quais bibliotecas de teste são utilizadas.
Explore a ferramenta antes de começar para se familiarizar com seu funcionamento.

Mais detalhes no GitHub da ferramenta: https://github.com/andrehora/testminer.

---

## Passo 1: Selecionar um repositório

Escolha um repositório real que possua testes de software.
Abaixo estão alguns links para ajudá-lo a encontrar projetos interessantes:

- Python: https://github.com/topics/python?l=python
- JavaScript: https://github.com/topics/javascript?l=javascript
- TypeScript: https://github.com/topics/typescript?l=typescript
- Java: https://github.com/topics/java?l=java

- Tópicos: [ai](https://andrehora.github.io/testminer/#topic:ai), [llm](https://andrehora.github.io/testminer/#topic:llm), [api](https://andrehora.github.io/testminer/#topic:api), [nodejs](https://andrehora.github.io/testminer/#topic:nodejs), [android](https://andrehora.github.io/testminer/#topic:android)

- Por organização: [Google](https://andrehora.github.io/testminer/#google), [Microsoft](https://andrehora.github.io/testminer/#microsoft), [Apple](https://andrehora.github.io/testminer/#apple), [Facebook](https://andrehora.github.io/testminer/#facebook), [Netflix](https://andrehora.github.io/testminer/#netflix), 
[GitHub](https://andrehora.github.io/testminer/#github), [Apache](https://andrehora.github.io/testminer/#apache), [HuggingFace](https://andrehora.github.io/testminer/#huggingface)

## Passo 2: Explorar o repositório selecionado

Busque o repositório escolhido no [TestMiner](https://andrehora.github.io/testminer) e analise os dados de teste gerados pela ferramenta.

## Passo 3: Explicar uma prática de teste

Escolha uma prática ou dado de teste relevante e explique com suas próprias palavras.

---

## Instruções de entrega

1. Faça um `fork` deste repositório (saiba mais sobre forks [aqui](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)).
2. Responda às questões abaixo diretamente neste arquivo `README.md` do seu fork. Pode adicionar imagens para enriquecer sua explicação.
3. No Moodle, submeta apenas a URL do seu fork.

---

## Respostas

Repositório: `https://github.com/microsoft/vscode`

URL TestMiner: `https://andrehora.github.io/testminer/#microsoft/vscode`

Explicação:

Uma prática de teste que se destaca nos dados do TestMiner para o VS Code é a **diversificação dos tipos de testes** (uma pirâmide de testes bem distribuída).

Em vez de depender apenas de testes unitários, o projeto divide seus testes em diferentes categorias para cobrir o sistema de ponta a ponta:

- **Testes unitários e de integração (3.803 arquivos):** validam a lógica interna de serviços, editores e extensões de forma rápida e isolada.
- **Testes End-to-End (776 arquivos) e Smoke Tests (78 arquivos):** simulam o uso real do editor via interface gráfica (usando Playwright e Electron), garantindo que a aplicação inicialize e execute os fluxos essenciais sem quebrar antes de uma release.
- **Snapshots (405 arquivos) e Fixtures (1.284 arquivos):** facilitam o teste de saídas visuais, sintaxe e comportamentos complexos com arquivos de exemplo reais, evitando asserções manuais repetitivas.

Essa diversidade é essencial em um projeto do tamanho do VS Code: os testes unitários garantem agilidade para quem desenvolve no dia a dia, enquanto os testes de fumaça e ponta a ponta trazem a segurança necessária para lançar novas versões com frequência.
