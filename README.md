# Sistema Acadêmico - Análise e Levantamento de Requisitos

> **Disciplina:** Gestão e Qualidade de Software  
> **Professor:** Daniel Henrique Matos de Paiva  
> **Instituição:** Centro Universitário UNA (2026)  

---

## 📌 1. Visão Geral do Projeto
O **Sistema Acadêmico** é uma plataforma desenvolvida para centralizar e otimizar os processos acadêmicos de alunos, professores e coordenação, reduzindo erros e ineficiências provenientes da gestão manual.

### Integrantes da Equipe
- **Albano de Souza** - RA: 32516336
- **Alice Fernandes Barbosa** - RA: 326128348
- **Ana Carolina de Sousa Freitas** - RA: 325132932
- **Débora Suellen Gomes** - RA: 325132368


---

## 🎯 2. Escopo e Requisitos

### Requisitos Funcionais (RF)
- **RF1:** Cadastro e gerenciamento de matrículas com validação automática de pré-requisitos.
- **RF2:** Lançamento de notas e frequência pelo professor no diário de classe digital.
- **RF3:** Geração automática de históricos acadêmicos com cálculo de média ponderada por créditos.
- **RF4:** Consulta de disciplinas disponíveis, vagas e pré-requisitos.

### Requisitos Não Funcionais (RNF)
- **RNF1 (Performance):** Tempo de resposta máximo de 2 segundos para consultas.
- **RNF2 (Disponibilidade):** SLA de 99,5% durante o período letivo.
- **RNF3 (Segurança):** Autenticação OAuth 2.0, criptografia de dados sensíveis e conformidade com LGPD.
- **RNF4 (Usabilidade):** Interface responsiva acessível em dispositivos desktop e mobile.

---

## 📐 3. Modelagem de Dados e Arquitetura
O banco de dados adotado é o **PostgreSQL**, estruturado até a 3ª Forma Normal (3FN).

Os diagramas e especificações detalhadas encontram-se na pasta `/docs`:
- **Modelo Entidade-Relacionamento (DER):** Mapeamento das entidades `Curso`, `Disciplina`, `Pré-requisito`, `Turma`, `Professor`, `Aluno`, `Matrícula`, `Nota` e `Histórico`.
- **Diagrama de Classes:** Representação das classes de domínio, atributos, métodos e associações.

---

## 🔀 4. Estratégia de Versionamento e Qualidade

- **Modelo de Branches:** [GitFlow](https://nvie.com/posts/a-successful-git-branching-model/) (`main`, `develop`, `feature/*`).
- **Convenções de Commit:** [Conventional Commits](https://www.conventionalcommits.org/) (`feat/`, `fix/`, `docs/`, `refactor/`).
- **Política de Code Review:** Aprovação obrigatória de pelo menos 2 revisores (Pull Request) antes do merge para a branch `main`.

---

## 🧪 5. Plano de Garantia da Qualidade (QA)
Foram estabelecidos cenários de teste para validação das regras críticas de negócio:
1. **Validação de Pré-requisito:** Bloqueio e exibição de alerta ao tentar realizar matrícula sem pré-requisito cumprido.
2. **Consistência de Notas:** Restrição do lançamento de notas fora do intervalo de 0 a 10.
3. **Emissão de Histórico:** Verificação da integridade das disciplinas cursadas e do cálculo correto da média ponderada por créditos.

---

## 📁 6. Estrutura do Repositório e Entregáveis

```text
├── docs/
│   ├── DER_Sistema_Academico.png
│   ├── Diagrama_de_Classes.png
│   ├── Trabalho_Sistema_Academico_ABNT.docx
│   └── Sistema_Academico_Apresentacao.pptx
└── README.md
