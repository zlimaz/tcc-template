# Trabalho de Conclusão de Curso (TCC) — Engenharia de Software / UnB-FGA

Repositório oficial para desenvolvimento da monografia de Trabalho de Conclusão de Curso (TCC) do curso de Engenharia de Software da **Universidade de Brasília (UnB)** — Faculdade UnB Gama (FGA).

---

## 📌 Identificação

* **Discente:** Miguel Arthur Oliveira de Lima
* **Orientador:** Prof. Dr. Hilmer Rodrigues Neri
* **Instituição:** Universidade de Brasília (UnB) — Faculdade UnB Gama (FGA)
* **Curso:** Bacharelado em Engenharia de Software
* **Área:** Engenharia de Software Experimental & Segurança da Informação

---

## 🎯 Tema e Escopo da Pesquisa

**Problema de Pesquisa:**
> A infraestrutura de desenvolvimento e homologação de plataformas digitais governamentais federais carece de monitoramento de segurança centralizado em tempo de execução, contrariando as exigências do Controle 8 do PPSI 2.0 e da NC 21 do GSI-PR, conforme evidenciado no Acórdão nº 2.387/2024 – TCU. Essa lacuna expõe um vetor crítico na cadeia de suprimentos de software governamental que permanece sem uma avaliação do seu grau de conformidade em tempo de execução.

**Questão de Pesquisa (GQM):**
> *Como avaliar o grau de conformidade da infraestrutura de monitoramento de segurança cibernética em tempo de execução de sistemas digitais da Administração Pública Federal conforme o Controle 8 do PPSI 2.0 e os requisitos da NC 21 do GSI-PR?*

**Metodologia:**
* **Estudo de Caso Único Incorporado (*Embedded Single-Case Study*)**, fundamentado nas diretrizes de Runeson e Höst (2009) e Yin (2015).
* **Revisão Estruturada da Literatura**, orientada pelo protocolo de Kitchenham e Charters (2007) e modelo PIO.

---

## 📂 Estrutura do Repositório

```text
├── docker-compose.yml           # Configuração de build e compilação do LaTeX em container
├── Dockerfile                   # Imagem Docker com TeX Live e pacotes abnTeX2
├── README.md                    # Documentação do repositório
├── OFICIAL/                     # Insumos normativos, diretrizes e matrizes de dados oficiais
│   ├── 19-SLR-guidelines.pdf    # Diretrizes de RSL (Kitchenham & Charters)
│   ├── Runeson e Host...pdf     # Diretrizes de Estudo de Caso em Engenharia de Software
│   ├── data_extraction(1).xls   # Matriz estruturada de extração dos 29 estudos primários
│   └── ...                      # Marcos regulatórios (PPSI 2.0, CIS Control 8, NC 21)
└── latex/                       # Código-fonte da monografia em LaTeX (abnTeX2)
    ├── Makefile                 # Automação de compilação (make, make clean)
    ├── tcc.tex                  # Arquivo principal do documento
    ├── bibliografia.bib         # Base de dados bibliográfica (.bib)
    ├── figuras/                 # Diagramas, fluxos e ilustrações vetoriais (.eps)
    ├── fixos/                   # Configurações institucionais da FGA/UnB e abnTeX2
    └── editaveis/               # Capítulos e seções editáveis do trabalho
        ├── introducao.tex            # Capítulo 1: Introdução, GQM, Metodologia e Cronograma
        ├── referencial_teorico.tex   # Capítulo 2: Fundamentação Teórico-Normativa
        └── revisao_estruturada.tex   # Capítulo 3: Revisão Estruturada da Literatura
```

---

## 🛠️ Como Compilar o Documento

### Pré-requisitos
* [Docker](https://docs.docker.com/engine/install/) e [Docker Compose](https://docs.docker.com/compose/install/) instalados.

### Compilação e Geração do PDF
Execute na raiz do projeto:
```bash
docker compose up
```
O documento compilado e formatado nos padrões ABNT/UnB estará disponível em:
📂 `latex/tcc.pdf`

### Limpeza de Arquivos Temporários
```bash
docker compose run --rm latex bash -c 'make clean'
```
