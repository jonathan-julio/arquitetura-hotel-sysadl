# Estilo arquitetural: Feedback Control Loop

O estilo arquitetural adotado para a parte de controle de acesso e Feedback Control Loop.

## Motivo da escolha

O Feedback Control Loop foi escolhido porque a parte de controle de acesso funciona como um ciclo: sensores e leitores coletam dados do ambiente, controladores analisam esses dados e atuadores modificam o ambiente por meio de liberacao ou bloqueio de acesso.

## Mapeamento no projeto

- Sensores/leitores: `LeitorDispositivoCP`, `SensorAcessoCP` e `AreaComumCP`.
- Controladores: `ControladorAcessoCP` e `ControladorAreaCP`.
- Atuador: `AtuadorPortaCP`.
- Conector sensor-controlador: `identificacaoHospedeCN`.
- Conector controlador-atuador: `controleAcessoCN`.
- Comportamento principal: `AutorizarAcessoAC`, apoiado por `DecidirAcessoAN` e `DecidirAcessoEQ`.

## Ciclo arquitetural

1. O leitor ou sensor coleta a identificacao ou solicitacao de acesso.
2. O controlador recebe os dados e decide se a regra de acesso permite a entrada.
3. O atuador recebe o comando e libera ou bloqueia a porta/catraca.
4. O resultado da atuacao afeta o ambiente, fechando o ciclo de controle.

## Qualidades favorecidas

- Desempenho: a decisao de acesso fica concentrada em um controlador claro.
- Disponibilidade: o controle pode operar com regras locais em caso de falha temporaria.
- Modificabilidade: novos sensores, leitores ou atuadores podem ser conectados ao ciclo.
