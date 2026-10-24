# Agente de Atendimento e Suporte — Portaria/Recepção

Prompt de sistema para um agente de IA de suporte à portaria/recepção: orienta sobre o sistema de portaria, procedimentos internos e falhas simples de software/hardware, com base documental. Inclui regra de emergência, classificação de risco, encaminhamento por falta de informação, confidencialidade e transparência.

## Visão geral

O arquivo [prompt_final.md] define o comportamento de um agente que apoia os funcionários do setor de portaria/recepção de uma instituição. A prioridade do agente é segurança, conformidade institucional, precisão e transparência: quando a informação não está documentada, ele diz isso e encaminha, em vez de inventar uma resposta.

## O que o agente faz

- Orienta sobre a operação do sistema de portaria, somente nas funcionalidades documentadas.
- Explica procedimentos internos e solicitações de terceiros, respeitando autorização e confidencialidade.
- Faz o suporte inicial de pequenas falhas de software e hardware, uma ação por vez.
- Identifica quando o caso deve ser encaminhado ao superior imediato ou à TI.

## Como o prompt está organizado

1. **Intenção:** papel do agente e o que ele não substitui (responsáveis técnicos, gestores, profissionais de saúde, equipes de emergência).
2. **Detalhes e contexto de atuação:** uso da base de conhecimento, atendimento do sistema, procedimentos institucionais e suporte inicial.
3. **Exemplos de comportamento esperado:** cinco situações (erro no sistema, informação não documentada, falha de hardware, emergência e informação ausente na base).
4. **Fluxo obrigatório de atendimento:** dez etapas, da identificação da solicitação até a indicação da fonte documental.
5. **Limites, segurança e regras inegociáveis:** proibição de inventar informações, classificação de risco, regra exclusiva para emergências, encaminhamento por falta de informação, confidencialidade e transparência.
6. **Padrão obrigatório das respostas:** Orientação, Resultado esperado, Risco, Fonte e Próximo passo.

## Regras principais

- **Emergência:** a resposta é somente o contato do número de emergência interno, sem texto adicional.
- **Sem invenção:** normas, menus, permissões, diagnósticos, prazos, responsáveis e contatos só são citados se estiverem documentados ou fornecidos.
- **Risco:** cada procedimento técnico é classificado como baixo, médio ou alto; procedimentos de risco alto exigem autorização e procedimento institucional.
- **Falta de informação:** o agente usa uma mensagem padrão que indica o superior imediato (questões administrativas) e a TI (questões técnicas).
- **Confidencialidade:** não divulga informações restritas e não solicita senhas ou credenciais.

## Como usar

1. Copie o conteúdo de `prompt_final.md` para o campo de instruções (prompt de sistema) da plataforma de agentes que você usa.
2. Substitua os placeholders pelos dados reais da instituição:
   - `[XY]`: nome da empresa;
   - `[XYZ]Portaria`: nome do sistema de portaria;
   - `[XYZ1]`, ramal `1111` e sala `XYZ11`: superior imediato;
   - ramal `2222` e sala `XYZ22`: TI;
   - `[193]`: número de emergência interno.
3. Carregue a base de conhecimento (manuais, normas, procedimentos e demais documentos) que o agente deve consultar.
4. Teste com os cenários dos exemplos do prompt antes de colocar em uso.

## Documentação do projeto

O arquivo [comparativo_opiniao.txt] compara a versão inicial do agente com a versão final entregue, em aspectos como objetivo, base de conhecimento, suporte técnico, emergências, encaminhamento, formato das respostas e fluxo de atendimento. Também traz os resultados qualitativos de sete testes práticos, a conclusão sobre a evolução do prompt e a opinião final do autor: um agente de IA exige avaliação, atualização e aprimoramento contínuos do prompt, guiados por critérios claros e testes.

O arquivo [prompt_1.md] reúne a primeira versão do prompt, para consulta e comparação com a versão final.

## Observações

- Os nomes, ramais e salas do prompt são placeholders, não dados reais.
- Não publique manuais, credenciais nem informações restritas da instituição neste repositório.
- O agente não substitui responsáveis técnicos, gestores, profissionais de saúde, equipes de emergência ou autoridades competentes.
