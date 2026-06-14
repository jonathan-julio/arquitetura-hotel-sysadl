# Projeto Hotel/Resort - 3a avaliacao

Versao da terceira avaliacao do projeto Hotel/Resort em SysADL.

Esta entrega apresenta a visao estrutural revisada e acrescenta a visao comportamental no `My.sysadl`, dentro do pacote `SysADL_components`.

O estilo arquitetural adotado para a parte de controle de acesso e **Feedback Control Loop**. Ele foi escolhido porque o sistema coleta informacoes por sensores/leitores, decide a autorizacao em controladores e aciona atuadores no ambiente.

## Visualizacoes esperadas no `representations.aird`

- Requirements Diagram
- Package Diagram
- BDD de tipos, portas, conectores e componentes
- IBD do `SistemaHotelResortCP`
- Allocation Table

## Comportamento no modelo

As definicoes comportamentais estao no `My.sysadl`:

- `RealizarCheckInAC`
- `AutorizarAcessoAC`
- `RealizarCheckOutAC`
- `RegistrarConsumoAC`

As imagens em `imagens/` servem como apoio visual para conferir e reproduzir as visoes estruturais e comportamentais do projeto.

## Estilo arquitetural

O mapeamento do Feedback Control Loop esta documentado em `docs/03_estilo_feedback_control_loop.md`.
