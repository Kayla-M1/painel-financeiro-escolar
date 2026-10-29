# Painel financeiro escolar (planilha automatizada + dashboard)

Planilha financeira que eu criei para uma escola de educação infantil pequena, com um painel web que mostra os números. Esta é a **versão de portfólio**: a estrutura e as fórmulas são as mesmas da planilha real, mas a escola, os alunos, os responsáveis e os valores são **fictícios**.

🔗 **Ver o painel:** https://kayla-m1.github.io/painel-financeiro-escolar/

## O problema

A escola ia começar a cobrar as mensalidades por boleto e controlava tudo à mão. A dona precisava saber, sem fazer conta:

- quanto entra e quanto sai em cada mês;
- quem está com boleto vencido e quanto deve com multa e juros;
- se o caixa fecha positivo no fim do ano.

## Resultado

A escola não tinha planilha. A diretora fazia apenas uma organização básica das contas. Com a planilha, que já está em uso, ela passou a ver mês a mês tudo o que entra e tudo o que a escola gasta.

## O que a planilha faz sozinha

| Aba | O que acontece |
|---|---|
| **Config** | Ano letivo, dia de vencimento, multa, juros, tarifa do boleto e valor da mensalidade de cada turma e das atividades extras (Judô e Balé) |
| **Alunos** | Ao cadastrar um aluno e escolher a turma, a mensalidade, as atividades e o desconto viram o valor do boleto |
| **Boletos** | Gera os 12 boletos do ano para cada aluno, respeitando o mês de entrada e de saída. O status muda sozinho (pago, vencido, a vencer ou cancelado) e calcula dias de atraso, multa e juros |
| **Despesas Fixas → Contas Fixas** | Cadastra uma vez (aluguel, salários, internet…) e a planilha lança nos 12 meses. Só é preciso marcar a data em que pagou |
| **Despesas / Outras Receitas** | Gastos e entradas avulsos (manutenção, festa, matrícula, uniforme…) |
| **Resumo** | Receitas, despesas, tarifas, resultado e saldo acumulado de cada mês, além de indicadores como inadimplência, alunos por turma e margem do ano. Um aviso no topo diz se há boleto vencido ou conta atrasada |
| **Pendências** | Lista sozinha os boletos vencidos e os cadastros sem CPF do responsável |
| **Alunos A-Z** | Lista em ordem alfabética que se atualiza sem bagunçar a aba de cadastro |

Também tem listas suspensas, validação de dados, cores por status e células de fórmula protegidas contra apagamento acidental.

## O painel

O `index.html` lê os números calculados pela planilha e mostra:

- indicadores do ano: receita, despesas, saldo em caixa, alunos ativos, inadimplência e margem;
- gráfico de receitas e despesas por mês com o saldo acumulado;
- despesas por categoria;
- tabela de boletos vencidos com o valor atualizado;
- status dos boletos mês a mês.

É um arquivo HTML único, sem bibliotecas externas, que funciona no celular e tem modo escuro.

## Arquivos

- `planilha-financeira-escola-demo.xlsx` – a planilha com dados fictícios. Abre no Excel ou no Google Planilhas.
- `index.html` – o painel.

## Como eu fiz

Montei a lógica da planilha e o painel com apoio de IA (Claude), testando as fórmulas com dados de exemplo até cobrir os casos reais: aluno que entra no meio do ano, aluno que sai, bolsista, desconto para irmãos, boleto cancelado e pagamento com atraso.

---
Feito por [Kayla Michelle Santos](https://github.com/Kayla-M1) · [LinkedIn](https://www.linkedin.com/in/kaylamichellesantos)
