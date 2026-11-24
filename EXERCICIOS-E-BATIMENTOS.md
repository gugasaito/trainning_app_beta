# v3.15.1 — Iniciar exercício e batimentos por exercício (FB-025)

Iniciar exercício registra o timestamp real nesta sessão. Iniciar outro encerra o anterior. Encerrar exercício deixa o intervalo seguinte sem marcação. Pausar/finalizar o treino também encerra o exercício ativo; após retomar, iniciar o exercício novamente cria outro intervalo. Séries e cargas continuam independentes e não são inferidas pelos horários. Descansos entre séries ficam no intervalo até encerrar ou trocar de exercício.

No Histórico há uma lista de intervalos e, no Horizonte, um seletor Treino completo/exercício. O eixo continua sendo o workout associado do Saúde. Os intervalos são destacados e cada amostra informa o exercício ou intervalo sem marcação. O filtro mostra média/mínima/máxima das amostras exibidas do exercício, não estatísticas completas do HealthKit. Seleção reduzida de até 180 pontos pode deixar exercícios curtos sem amostras; nunca estimamos batimentos para preencher lacunas. Um ponto na fronteira pertence ao exercício que começa naquele instante, sem dupla contagem.

O gráfico depende de finalizar o workout no Watch/Fitness, disponibilizá-lo no Saúde e sincronizar/associar no Tracker. Não é leitura ao vivo. Sessões antigas não ganham intervalos automaticamente. Backups e sincronização preservam os novos intervalos por conta, incluindo exclusão/restauração. Até 1000 intervalos por sessão; horários fora da sessão, sobrepostos ou de outro treino são rejeitados.

Atualização somente Web. O nativo v3.14 já fornece amostras necessárias; não substituir arquivos Swift nem reautorizar permissões novas para esta demanda. Fechar e reabrir janelas antigas antes de registrar novos intervalos, para evitar editar os novos metadados com versões anteriores.

Cada exercício tem check manual Exercício executado. Marcar/desmarcar não inicia ou encerra intervalos, não altera séries nem pausa o treino. O check é independente por sessão, preservado em backup e sincronização; pode ser corrigido em Histórico → Editar de uma sessão. O Histórico lista os nomes marcados. Sessões antigas não recebem checks por inferência.
