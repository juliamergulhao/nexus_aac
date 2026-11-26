# NEXUS — Portal de Atividades Acadêmicas Complementares

Projeto acadêmico desenvolvido para apoiar estudantes no acompanhamento das Atividades Acadêmicas Complementares (AAC), reunindo consulta de progresso, registro de atividades, orientações e um assistente virtual baseado em regras.

## Estrutura

- `NEXUS_index.html` — interface do estudante.
- `NEXUS_admin.html` — painel administrativo para visualizar feedbacks e gerenciar regras do assistente.
- `README.md` — documentação do projeto.

## Como executar

1. Baixe ou clone este repositório.
2. Abra `NEXUS_index.html` em um navegador atualizado.
3. Para acessar o painel administrativo, abra `NEXUS_admin.html`.
4. Senha demonstrativa do painel: `NEXUS2026`.

> O projeto é um protótipo front-end. Não exige instalação de dependências ou servidor para a demonstração local.

## Funcionalidades

### Portal do estudante
- Visão geral da carga horária e progresso de AAC.
- Consulta e pesquisa de atividades registradas.
- Cadastro de novas atividades com categoria, data, carga horária e instituição.
- Campo para selecionar comprovante/certificado.
- Área de documentos e orientações.
- Assistente virtual para dúvidas frequentes sobre AAC.
- Avaliação das respostas do assistente com 👍 ou 👎.

### Painel administrativo
- Indicadores de feedbacks positivos e negativos.
- Consulta ao histórico de feedbacks.
- Cadastro, edição e gerenciamento de regras personalizadas.
- Priorização de regras por peso.
- Teste de perguntas para observar a regra selecionada e a resposta.
- Exportação de feedbacks em CSV.
- Exportação e importação de backup em JSON.

## Lógica do assistente

O assistente compara a pergunta enviada com palavras-chave e expressões cadastradas nas regras. A seleção considera correspondência de termos, cobertura das palavras-chave, correspondência de frases, especificidade e prioridade/peso da regra. A regra mais adequada é escolhida para compor a resposta.

O mecanismo é baseado em regras, não em um modelo de inteligência artificial generativa. O feedback negativo registra uma avaliação para análise. A melhoria da base ocorre por intervenção administrativa: uma pessoa revisa o feedback e cria ou ajusta uma regra.

## Persistência de dados e limitações

Os dados de atividades, regras e feedbacks são armazenados no `localStorage` do navegador. Por isso, o conteúdo fica associado ao navegador e à origem em que as páginas são abertas; não existe sincronização automática entre computadores ou usuários. O painel oferece exportação/importação de backup para transferência manual.

O seletor de arquivo de certificado faz parte do protótipo; o projeto não possui backend para enviar e armazenar o arquivo em um servidor. A senha do painel está no código front-end e funciona apenas como barreira visual de demonstração, não como autenticação segura.

## Demonstração sugerida

1. Abra o portal e faça uma pergunta sobre horas pendentes ou documentos.
2. Avalie a resposta com 👍 ou 👎.
3. Abra o painel administrativo e consulte o feedback registrado (no mesmo navegador/origem).
4. Ajuste ou cadastre uma regra com palavras-chave, resposta e prioridade.
5. Volte ao portal e repita a pergunta para observar a regra atualizada.

## Tecnologias

- HTML5
- CSS3
- JavaScript
- Web Storage API (`localStorage`)
- CSV e JSON para exportação de dados

## Observação acadêmica

Os valores exibidos no painel (como 140 horas concluídas de 200 horas) são dados demonstrativos do protótipo e não representam consulta a um sistema acadêmico oficial. Os critérios efetivos de AAC devem ser confirmados no regulamento vigente do curso.
