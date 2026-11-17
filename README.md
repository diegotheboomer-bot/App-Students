# VELA: Virtual Education & Learning Analytics (demo)

Demo de uma app em que os alunos fazem testes no telemóvel ou no computador, a correção é automática e o professor cria testes com IA ou a partir de um PDF. Pensada primeiro para escolas portuguesas.

## Abrir

É um único ficheiro, sem instalação: abre `index.html` no browser. Para ver o professor e o aluno ao mesmo tempo, abre-o em dois separadores.

## Perfis

- **Direção**: vê todas as turmas, professores e pautas. Escolhe a escala (valores de 0 a 20, percentagem e menção, ou níveis de 1 a 5), se os professores aprovam quem entra e o código da escola.
- **Professor**: cria testes (IA, importar ficheiro ou à mão), aceita pedidos de entrada, **abre o teste na aula** (o tempo começa a contar para todos), acompanha ao vivo, dá mais tempo ou termina, corrige o desenvolvimento e vê a pauta.
- **Aluno**: pede para entrar em turmas com código, faz testes e vê as notas. Mudar de separador, de app ou de janela fica registado.

## Notas e perguntas protegidas

- Depois de o teste terminar, os alunos não veem a nota nem as perguntas até o professor carregar em **Mostrar notas aos alunos**.
- As perguntas e as respostas certas têm um interruptor à parte (**Mostrar também as perguntas**). Se outra turma ainda vai fazer o mesmo teste, a VELA avisa antes.

## Um teste para várias turmas

- No editor, escolhe-se mais do que uma turma. Cada turma fica com o seu teste, que o professor abre na respetiva aula, um de cada vez.
- Alterações às perguntas passam para as turmas que ainda não fizeram o teste.

## Trabalhos, notas sem teste e mensagens

- **Trabalhos**: o professor define instruções, prazo e o que se entrega (ficheiro, fotografia, link). Os alunos juntam PDFs, Word, Excel, fotografias ou links; o professor vê cada entrega e dá nota e comentário.
- **Nota sem teste**: para testes em papel, apresentações orais ou participação. O professor escreve a nota de cada aluno.
- Testes, trabalhos e notas sem teste contam todos para a **média da disciplina**, com os **critérios de avaliação** que a Direção define (por omissão: testes 60%, trabalhos 30%, outras 10%). A **média geral** é a média das disciplinas.
- **Corrigir uma a uma**: o professor percorre as entregas e os testes aluno a aluno, com setas para o anterior e o seguinte.
- **Fotografia de perfil**: cada pessoa pode pôr uma fotografia em Definições; sem fotografia aparecem as iniciais.
- **Mural da turma**: avisos do professor, trabalhos novos e testes marcados, com comentários de toda a turma. Cada trabalho tem também comentários da turma.
- **Entregar trabalhos**: um botão «Adicionar trabalho» mostra as opções em bolhas (ficheiro, fotografia, link, mensagem).
- **Mensagens**: conversa privada entre cada aluno e o professor de cada turma.
- **Definições**: tema (automático, claro, escuro), letra maior e avisos.

## Análise e correção manual

- **Análise**: acerto por pergunta, por tipo e por tema, opções escolhidas em cada escolha múltipla, conceitos usados nas respostas de desenvolvimento e alerta de **respostas muito semelhantes** entre alunos.
- **Correção**: mudar a resposta certa, aceitar respostas curtas que ficaram de fora ou mudar os pontos de qualquer pergunta de um aluno. As notas são recalculadas logo.

## Imagens nas perguntas

- Ao importar um PDF, a figura de cada pergunta é encontrada e recortada automaticamente (zona com desenho que não é texto, mais os rótulos à volta).
- O professor pode adicionar, colar (Ctrl+V), trocar e recortar imagens, incluindo recorte quadrado.
- Os alunos veem a figura na pergunta e podem ampliá-la.

## O que é simulado

- **IA**: as perguntas "geradas" vêm de um pequeno banco de exemplo.
- **Importar**: PDFs com texto e `.txt` são lidos a sério (pdf.js). Word e fotografias de testes precisam de OCR/IA na versão real.
- **Desenvolvimento**: a nota sugerida usa palavras-chave e o professor confirma sempre.
- **Contas e dados**: não há servidor nem login; tudo fica no `localStorage` do browser.
- **Saídas**: um browser deteta mudança de separador ou janela, mas não um segundo dispositivo. Numa app nativa pode usar-se o Acesso Guiado (iOS) ou a Fixação de ecrã (Android).
