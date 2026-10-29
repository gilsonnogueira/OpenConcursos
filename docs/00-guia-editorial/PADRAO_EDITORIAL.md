# 📐 Manual de Padrão Editorial e Nomenclatura (OpenConcursos)

Este manual estabelece as diretrizes canônicas, estruturais e estilísticas para todos os verbetes e tratados de estudo do **OpenConcursos**. 

A padronização editorial é absoluta: **nenhum arquivo pode adotar nomenclaturas divergentes, cabeçalhos informais ou estruturas idiossincráticas**. O objetivo é garantir um material com densidade técnica de publicação profissional, livre de prolixidade e clichês de inteligência artificial.

---

## 1. Nomenclatura de Pastas e Arquivos

* **Padrão Kebab-case Numérico:** Pastas e arquivos utilizam prefixo numérico de dois dígitos e palavras em minúsculas separadas por hífen (`kebab-case`), sem acentos ou caracteres especiais.
  * Pasta: `docs/19-auditoria/01-fundamentos-e-normas-profissionais/`
  * Arquivo: `01-estrutura-conceitual-nbc-ta-200.md`
* **Correspondência Canônica:** O nome do arquivo deve refletir exatamente o escopo temático e a base normativa tratada.

---

## 2. Frontmatter YAML Obrigatório

Todo arquivo Markdown de conteúdo DEVE iniciar estritamente na linha 1 com o bloco YAML delimitado por `---`:

```yaml
---
id: AUD-01-01
titulo: "Estrutura Conceitual de Asseguração e Objetivos Gerais do Auditor Independente (NBC TA Estrutura Conceitual, NBC TO 3000 e NBC TA 200)"
disciplina: "Auditoria"
eixo: "01 - Fundamentos e Normas Profissionais"
bancas_prioritarias: ["FGV", "Cebraspe", "FCC"]
relevancia_edital: "Crítica"
ultima_revisao: "2026-10-29"
tags: ["nbc-ta-200", "asseguracao", "risco-de-auditoria", "ceticismo-profissional", "teoria-da-agencia"]
---
```

### Regras dos Campos do Frontmatter:
1. `id`: Código alfanumérico estrito no formato `[SIGLA]-[EIXO]-[ARQUIVO]`.
   * Exemplos: `AUD-01-01`, `AUD-03-04`, `AUD-06-02`.
   * Proibido usar códigos livres como `AUD-301`, `AUD-INT-01` ou similares.
2. `titulo`: Nome técnico, canônico e completo do verbete, **idêntico ao título H1**, sem aspas desnecessárias e **sem numeração prefixada** (como "01." ou "02.").
3. `disciplina`: Nome formal da disciplina (ex: `"Auditoria"`).
4. `eixo`: Nome oficial da pasta correspondente com seu número (ex: `"01 - Fundamentos e Normas Profissionais"`).
5. `bancas_prioritarias`: Lista com as principais bancas examinadoras do certame (`["FGV", "Cebraspe", "FCC"]`).
6. `relevancia_edital`: Nível de incidência em provas fiscais e de controle (`"Crítica"`, `"Altíssima"`, `"Alta"` ou `"Média"`).
7. `ultima_revisao`: Data no formato ISO `AAAA-MM-DD`.
8. `tags`: Array de palavras-chave padronizadas em `kebab-case`.

---

## 3. Título Principal (H1) e Síntese de Abertura (Lead)

O documento inicia imediatamente após o YAML:

```markdown
# [Título Canônico do Assunto sem Prefixo Numérico]

> [Parágrafo de síntese de alto nível definindo o objeto nuclear, a fundamentação legal/normativa primária e a consequência prática imediata para provas de alto rendimento. Deve estar em parágrafo único com blockquote simples '>'.]

---
```

### Regras de Abertura:
* **Proibido Prefixar Números no H1:** Use `# Estrutura Conceitual...` em vez de `# 01. Estrutura Conceitual...`.
* **Proibido Citações Duplas:** Nunca use `> >` ou múltiplos marcadores de citação empilhados. Use apenas `>`.
* **Proibido Rótulos Artificiais no Lead:** Não use `> **BLUF:**` ou `> **Resumo Executivo (BLUF):**`. O parágrafo em itálico/destaque no topo já cumpre visual e pedagogicamente a função de abertura executiva.

---

## 4. Seções Teóricas, Tabelas e Diagramas

1. **Numeração Sequencial de Tópicos:**
   * Títulos principais em H2: `## 1. [Tema]`, `## 2. [Tema]`, etc.
   * Subtópicos em H3: `### 1.1 [Subtema]`, etc.
2. **Linguagem Técnica e Sóbria (Zero IA Cliché):**
   * É proibido o uso de chavões sensacionalistas como *"Dissecação Cirúrgica"*, *"Regra de Ouro Inviolável"*, *"Casca de Banana Mortal"*.
   * Utilize termos editoriais padrão: *"Análise Normativa"*, *"Aspectos Críticos para Provas"*, *"Matriz Comparativa"*.
3. **Caixas de Alerta e Memorização:**
   * Padronizadas exclusivamente como:
     ```markdown
     > **Fique Ligado:** [Texto objetivo, pontual e direto destacando a pegadinha ou detalhe normativo de maior cobrança pela banca.]
     ```
   * Posicionamento: Imediatamente antes do divisor horizontal `---` de finalização da seção.
4. **Diagramas Visuais:**
   * Devem ser elaborados nativamente em blocos `mermaid` (flowcharts, sequence diagrams ou state diagrams), sempre testados e válidos.

---

## 5. Seção Canônica de Questões de Provas

A seção de treino prático deve seguir estritamente o padrão abaixo em TODOS os arquivos:

### 5.1 Título da Seção
Sempre nomeada de forma uniforme:
```markdown
## [N]. Questões Paradigmáticas Aplicadas
```
*(Proibido usar variações como "Bateria de Questões Oficiais Comentadas Alternativa por Alternativa" ou "Questões Oficiais Comentadas (QConcursos)").*

### 5.2 Cabeçalho de Questão
O cabeçalho deve conter o link clicável direto para a questão no portal QConcursos:
```markdown
### [Questão XX](https://www.qconcursos.com/questoes-de-concursos/questoes/...) — [Banca — Órgão / Cargo — Ano]
```
* O texto do link é estritamente `[Questão XX](URL)`.
* O separador entre o link e a identificação do concurso é o travessão com espaços: ` — `.

### 5.3 Enunciado e Alternativas
```markdown
**Enunciado:**  
[Texto integral e fiel do enunciado oficial da questão da prova.]

* (A) [Texto da alternativa A]
* (B) [Texto da alternativa B]
* (C) [Texto da alternativa C]
* (D) [Texto da alternativa D]
* (E) [Texto da alternativa E]
```
*(Para questões no estilo Cebraspe de Certo/Errado, utilize `* ( ) Certo` e `* ( ) Errado` ou os itens numerados romanos).*

### 5.4 Gabarito Oficial
Deve ser inserido em cabeçalho H4 limpo e padronizado:
```markdown
#### Gabarito: **X**
```
*(Onde X é a letra `A`, `B`, `C`, `D`, `E` ou `Certo` / `Errado`).*
* **Proibido:** `#### Gabarito e Dissecação Técnica: **Alternativa X**`.
* **Proibido:** `**Gabarito Oficial:** **X**`.
* **Proibido:** `Gabarito Oficial: X`.

### 5.5 Comentários das Alternativas (Sem Prolixidade)
* **Eliminação de Cabeçalhos Intermediários:** É terminantemente PROIBIDO inserir linhas como `**Comentário Analítico Alternativa por Alternativa:**` ou `**Análise Detalhada das Alternativas:**`. O fluxo deve seguir diretamente de `#### Gabarito: **X**` para os marcadores de lista.
* **Marcadores de Alternativas:**
  ```markdown
  * **A (Errada):** [Justificativa técnica concisa apontando a violação normativa ou fática.]
  * **B (Errada):** [Justificativa técnica concisa.]
  * **C (Certa):** [Fundamentação na norma/jurisprudência que valida o gabarito.]
  * **D (Errada):** [Justificativa técnica concisa.]
  * **E (Errada):** [Justificativa técnica concisa.]
  ```
* **Terminologia Obrigatória:**
  * Use SEMPRE **`(Errada)`** ou **`(Errado)`** e **`(Certa)`** ou **`(Certo)`**.
  * É PROIBIDO usar *"Incorreta"* ou *"Incorreto"*.
  * Para itens isolados, utilize: `* **Item I (Certo):**` e `* **Item II (Errado):**`.

### 5.6 Destaque da Questão e Separador
Ao final dos comentários de cada questão, pode-se inserir um resumo mnemônico ou alerta:
```markdown
> **Fique Ligado:** [Regra de ouro cobrada na questão para rápida fixação mental.]

---
```

---

## 6. Seção Final de Navegação

Todo verbete finaliza com a seção de encadeamento pedagógico:

```markdown
---

## [N+1]. Verbetes Conexos & Próximos Passos

- 🔗 [Título do Verbete Anterior](link-relativo-anterior.md)
- 🔗 [Título do Verbete Subsequente](link-relativo-proximo.md)
```

---

## 7. Checklist de Conformidade Editorial (Auditoria Pré-Commit)

Antes de aprovar qualquer alteração ou novo arquivo, execute a verificação dos seguintes itens:

- [ ] Arquivo possui frontmatter YAML completo iniciando na linha 1 com delimitadores `---`.
- [ ] O `id` segue o padrão exato `AUD-XX-YY`.
- [ ] O `titulo` no YAML é rigorosamente idêntico ao título `# [H1]` do corpo.
- [ ] O título H1 NÃO possui numeração prefixada (ex: sem `01. `).
- [ ] O parágrafo de abertura está em blockquote simples (`>`) sem rótulo `BLUF:` e sem citação dupla (`> >`).
- [ ] Ausência total do termo `**Comentário Analítico Alternativa por Alternativa:**`.
- [ ] Ausência total de `Gabarito Oficial:`. Todas as questões usam `#### Gabarito: **X**`.
- [ ] As alternativas usam a nomenclatura `(Errada)` / `(Certa)` e NÃO `(Incorreta)`.
- [ ] A seção de questões chama-se exatamente `## [N]. Questões Paradigmáticas Aplicadas`.
- [ ] Todos os cabeçalhos de questão possuem link markdown clicável no formato `### [Questão XX](URL) — [Banca — Órgão / Cargo — Ano]`.
- [ ] Diagramas Mermaid compilam sem erros de sintaxe.
