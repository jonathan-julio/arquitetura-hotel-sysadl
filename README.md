# Arquitetura Hotel/Resort em SysADL

Este repositorio reune a modelagem arquitetural de um sistema para hotel/resort usando SysADL. O projeto considera funcionalidades como reserva, check-in, check-out, controle de acesso, consumo de servicos, uso de areas comuns e pagamento.

O objetivo principal e mostrar a evolucao da arquitetura entre uma versao inicial, focada em requisitos e estrutura, e uma versao revisada, com comportamento e estilo arquitetural.

## Organizacao do repositorio

```text
.
├── primeiraunidade/
│   ├── My.sysadl
│   ├── README.md
│   └── representations.aird
├── terceiraunidade/
│   ├── My.sysadl
│   ├── README.md
│   └── representations.aird
├── 01_o_que_mudou.md
├── 02_visao_comportamental.md
├── 03_estilo_feedback_control_loop.md
└── comparativo_primeira_terceira_unidade.docx
```

## Primeira unidade

A pasta `primeiraunidade/` contem a versao inicial do projeto. Essa etapa concentra a modelagem nos requisitos e na visao estrutural do sistema.

Principais elementos:

- modelo de requisitos;
- tipos iniciais;
- portas;
- conectores;
- componentes;
- configuracao estrutural principal do sistema.

Essa versao serve como base arquitetural inicial. Ela mostra quais elementos compoem o sistema e como esses elementos se relacionam estruturalmente.

## Terceira unidade

A pasta `terceiraunidade/` contem a evolucao do projeto. Nessa etapa, a estrutura inicial foi revisada e o modelo passou a incluir a visao comportamental.

Principais elementos:

- requisitos revisados;
- visao estrutural refinada;
- behaviors/activities para os fluxos principais;
- actions, constraints/equations e executables;
- allocations relacionando comportamento e estrutura;
- estilo arquitetural Feedback Control Loop aplicado ao controle de acesso.

A terceira unidade preserva a base da primeira, mas detalha melhor as responsabilidades dos componentes e o comportamento esperado nos fluxos principais do hotel/resort.

## Documentos auxiliares

Os documentos na raiz ajudam a entender a evolucao do projeto:

- `01_o_que_mudou.md`: resume as principais mudancas entre a primeira e a terceira unidade.
- `02_visao_comportamental.md`: apresenta os comportamentos modelados na terceira unidade.
- `03_estilo_feedback_control_loop.md`: explica o estilo arquitetural adotado para o controle de acesso.
- `comparativo_primeira_terceira_unidade.docx`: documento comparativo mais completo entre as duas entregas.

## Leitura recomendada

Para entender o projeto de forma sequencial:

1. Ler `primeiraunidade/README.md`.
2. Abrir `primeiraunidade/My.sysadl` e observar a estrutura inicial.
3. Ler `terceiraunidade/README.md`.
4. Abrir `terceiraunidade/My.sysadl` e comparar a estrutura revisada com a primeira versao.
5. Ler `01_o_que_mudou.md`, `02_visao_comportamental.md` e `03_estilo_feedback_control_loop.md`.
6. Usar `comparativo_primeira_terceira_unidade.docx` como resumo final da evolucao.

## Resumo da evolucao

A primeira unidade apresenta a base do sistema: requisitos e organizacao estrutural. A terceira unidade evolui essa base com revisao dos requisitos, maior clareza nas responsabilidades arquiteturais e inclusao de comportamento.

O controle de acesso foi interpretado como um ciclo de feedback: sensores e leitores coletam dados, controladores analisam regras e atuadores executam a liberacao ou o bloqueio de acesso. Essa organizacao ajuda a explicar a separacao entre coleta, decisao e atuacao dentro da arquitetura.
