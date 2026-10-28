# 📘 Guia de Contribuição e Boas Práticas

Seja bem-vindo à comunidade de curadores do **OpenConcursos**!

Nosso objetivo é construir o maior repositório aberto, atualizado e de alta densidade cognitiva para estudantes de concursos de alto rendimento no Brasil.

---

## 🛠️ Como Contribuir

### 1. Reportar Erratas ou Mudanças de Leis (Issues)
Se você encontrou:
- Uma lei ou artigo revogado;
- Uma súmula cancelada ou superada;
- Uma nova jurisprudência vinculante de tribunal superior;
- Um erro material ou de digitação em algum verbete;

Abra uma [**Nova Issue**](../../issues) descrevendo o arquivo, a linha e o fundamento oficial da alteração.

### 2. Propor ou Atualizar um Verbete (Pull Request)
1. Faça um **Fork** deste repositório.
2. Crie uma branch para a sua alteração: `git checkout -b feature/tributario-reforma`.
3. Crie ou edite o verbete seguindo rigorosamente o [`TEMPLATE_VERBETE.md`](TEMPLATE_VERBETE.md) e as diretrizes do [`METODO_ANTIPLAGIO.md`](METODO_ANTIPLAGIO.md).
4. Certifique-se de que todos os diagramas Mermaid compilam sem erros.
5. Faça o commit das alterações: `git commit -m "feat(tributario): adiciona verbete sobre regime de transicao da EC 132"`.
6. Envie para o seu fork: `git push origin feature/tributario-reforma`.
7. Abra um **Pull Request** detalhando as fontes primárias consultadas.

---

## 📐 Padrões de Estilo e Nomenclatura

* **Nome dos Arquivos:** Use apenas letras minúsculas separadas por hífen (`kebab-case`), sem acentos, cedilhas ou caracteres especiais (ex: `credito-tributario-suspensao.md`).
* **Frontmatter Obrigatório:** Todos os arquivos de notas devem começar com o bloco YAML contendo: `id`, `titulo`, `disciplina`, `bancas_prioritarias`, `relevancia_edital`, `ultima_revisao`, `tags`.
* **Zero Prolixidade:** Não use saudações, despedidas ou parágrafos de transição vazios. Vá direto ao ponto.
* **Diagramas em Mermaid:** Use diagramas nativos para processos e linhas do tempo em vez de imagens PNG/JPG estáticas.
