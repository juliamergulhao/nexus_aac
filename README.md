<div align="center">

# ✧ NEXUS
### Portal Virtual de Atividades Acadêmicas Complementares

**Uma solução web para organizar, acompanhar e orientar estudantes na gestão das Atividades Acadêmicas Complementares (AAC).**

<p>
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=222222" alt="JavaScript">
  <img src="https://img.shields.io/badge/localStorage-6C63B5?style=for-the-badge&logo=googlechrome&logoColor=white" alt="localStorage">
</p>

<p>
  <a href="NEXUS_index.html"><strong>✧ Portal do estudante</strong></a>
  &nbsp;·&nbsp;
  <a href="NEXUS_admin.html"><strong>⚙ Painel administrativo</strong></a>
  &nbsp;·&nbsp;
  <a href="Relatorio_NEXUS.docx"><strong>▤ Relatório</strong></a>
  &nbsp;·&nbsp;
  <a href="Apresentacao_NEXUS.html"><strong>▣ Apresentação</strong></a>
</p>

</div>

---

## 📌 Sobre o projeto

O **NEXUS** é um projeto acadêmico desenvolvido para apoiar estudantes no acompanhamento das Atividades Acadêmicas Complementares. A aplicação reúne, em um único ambiente, recursos para consultar o progresso, registrar atividades, acessar orientações e esclarecer dúvidas frequentes por meio de um assistente virtual baseado em regras.

O projeto também possui um painel administrativo para acompanhar as avaliações dos estudantes e manter a base de conhecimento do assistente atualizada.

## 🎯 Objetivos

- Centralizar informações relacionadas às Atividades Acadêmicas Complementares.
- Facilitar o acompanhamento de horas concluídas e pendentes.
- Organizar o registro de atividades e suas respectivas informações.
- Disponibilizar orientações e respostas para dúvidas recorrentes.
- Demonstrar um processo de melhoria contínua por meio de feedback e revisão das regras.

## 🖥️ Módulos da aplicação

### 1. Portal do estudante — `NEXUS_index.html`

- **Visão geral:** indicadores demonstrativos de carga horária e progresso.
- **Minhas atividades:** consulta, pesquisa e cadastro de atividades.
- **Documentos e orientações:** informações sobre certificados, categorias e acompanhamento.
- **Assistente virtual:** respostas para dúvidas frequentes sobre AAC.
- **Feedback:** avaliação das respostas com 👍 ou 👎.

### 2. Painel administrativo — `NEXUS_admin.html`

- Dashboard com indicadores de feedbacks.
- Histórico de avaliações dos estudantes.
- Cadastro, edição e gerenciamento de regras personalizadas.
- Configuração da prioridade/peso das regras.
- Teste de perguntas para verificar a regra selecionada e a resposta.
- Exportação de feedbacks em CSV.
- Exportação e importação de backup em JSON.

## 🧠 Como funciona o assistente virtual

O assistente utiliza uma **base de conhecimento composta por regras**. Cada regra possui informações como nome, palavras-chave, resposta e prioridade.

Quando o estudante envia uma pergunta, o sistema:

1. Normaliza o texto recebido.
2. Compara a pergunta com as palavras-chave e expressões das regras.
3. Calcula uma pontuação considerando correspondências, cobertura dos termos, especificidade e prioridade.
4. Seleciona a regra mais adequada.
5. Apresenta a resposta associada à regra selecionada.

### Ciclo de feedback e melhoria

```text
Pergunta do estudante
        ↓
Seleção da regra e resposta
        ↓
Avaliação com 👍 ou 👎
        ↓
Registro do feedback
        ↓
Análise pelo administrador
        ↓
Ajuste manual da regra
        ↓
Nova resposta nas próximas consultas
```

> **Importante:** o feedback não realiza treinamento automático de um modelo de IA. Ele registra uma avaliação para análise; a melhoria é feita manualmente pelo administrador, que revisa palavras-chave, resposta ou prioridade da regra.

## 🏗️ Estrutura do repositório

```text
nexus_aac/
│
├── NEXUS_index.html          # Portal do estudante
├── NEXUS_admin.html          # Painel administrativo
├── Apresentacao_NEXUS.html   # Apresentação interativa do projeto
├── Relatorio_NEXUS.docx     # Relatório acadêmico
└── README.md                 # Documentação do projeto
```

## 🚀 Como executar

A aplicação é um protótipo front-end e não exige instalação de dependências.

1. Faça o download ou clone este repositório.
2. Abra `NEXUS_index.html` em um navegador atualizado.
3. Para acessar a administração, abra `NEXUS_admin.html`.
4. Utilize a senha demonstrativa do painel: `NEXUS2026`.

### Executar com Git

```bash
git clone https://github.com/juliamergulhao/nexus_aac.git
cd nexus_aac
```

Em seguida, abra os arquivos HTML diretamente no navegador.

## 🧰 Tecnologias e recursos

| Tecnologia | Aplicação no projeto |
|---|---|
| HTML5 | Estrutura das interfaces |
| CSS3 | Identidade visual, componentes e responsividade |
| JavaScript | Interações, validações, pontuação e gerenciamento das regras |
| Web Storage API | Persistência de dados com `localStorage` |
| CSV | Exportação do histórico de feedbacks |
| JSON | Backup e transferência manual de dados |
| Git e GitHub | Versionamento e documentação do projeto |

## 💾 Armazenamento e limitações técnicas

- Atividades, feedbacks e regras são armazenados no `localStorage` do navegador.
- Os dados ficam associados ao navegador e à origem utilizada; não há sincronização automática entre computadores ou usuários.
- O painel oferece exportação e importação de backup em JSON.
- O campo de certificado permite selecionar um arquivo na interface, mas não existe backend para upload e armazenamento remoto.
- A senha do painel está no código front-end e serve apenas como barreira visual de demonstração, não como autenticação segura.
- Os números apresentados no painel, como 140 horas concluídas de um total de 200 horas, são dados demonstrativos e não representam consulta a um sistema acadêmico oficial.

## 🔮 Melhorias futuras

- Implementar backend e banco de dados centralizado.
- Criar autenticação real e controle de acesso por perfil.
- Implementar upload e armazenamento seguro de certificados.
- Integrar o portal a sistemas acadêmicos institucionais.
- Criar histórico de auditoria para alterações realizadas no painel.
- Disponibilizar relatórios de acompanhamento e indicadores administrativos.

## 📚 Documentação do projeto

- [Abrir o portal do estudante](NEXUS_index.html)
- [Abrir o painel administrativo](NEXUS_admin.html)
- [Consultar o relatório acadêmico](Relatorio_NEXUS.docx)
- [Abrir a apresentação interativa](Apresentacao_NEXUS.html)

## 👩‍💻 Autoria

**Julia Mergulhão Nunes**  
RA: 12526132193  
Curso: Gestão de Tecnologia da Informação  
Universidade Anhembi Morumbi  
Professor: Douglas da Silva Santos

---

<div align="center">

**NEXUS · Universidade Anhembi Morumbi**

*Projeto acadêmico — 2026*

</div>
