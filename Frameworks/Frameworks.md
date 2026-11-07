# Frameworks de engenharia de prompts

## CLEAR

Ajuda a escrever pedidos **claros e ajustáveis**. É útil quando a tarefa
precisa ser objetiva, mas a resposta deve considerar o público e permitir
revisão do resultado.

- **C — Concise (conciso):** vá direto ao pedido, sem informações desnecessárias.
- **L — Logical (lógico):** organize contexto, tarefa e saída em uma ordem clara.
- **E — Explicit (explícito):** diga exatamente o que espera da resposta.
- **A — Adaptive (adaptável):** ajuste a linguagem e o nível de detalhe ao público.
- **R — Reflective (reflexivo):** peça uma conferência da resposta antes de concluir.

### Exemplo

```txt
[CLEAR]

Você é um engenheiro de software especializado em manutenção de sistemas legados.

Explique como refatorar o código em Java para aplicar boas práticas de Clean Code.

Use uma linguagem clara, sem jargões excessivos. Pois o público são
desenvolvedores juniores que estão aprendendo a lidar com código legado.

Responda mostrando uma versão antes e depois da refatoração.

[CÓDIGO]
```

## CRISPE

Organiza **especialidade, cenário, tarefa e estilo de resposta**. É útil em
pedidos técnicos que exigem contexto e mais de uma alternativa de solução.

- **C — Capacity (capacidade):** defina a especialidade necessária.
- **R — Role (papel):** indique o papel que a IA deve assumir.
- **I — Insight (contexto):** forneça informações relevantes sobre o problema.
- **S — Statement (tarefa):** descreva o que deve ser feito.
- **P — Personality (estilo):** escolha como a resposta deve ser apresentada.
- **E — Experiment (experimento):** peça alternativas para comparar abordagens.

### Exemplo

```txt
[CRISPE]

[Capacity e Role]
Você é um engenheiro de software sênior especializado em migração e refatoração
de código legado em Python.

[Insight]
O sistema foi escrito originalmente em Python 2.7 e agora precisa ser
atualizado para Python 3.12, garantindo compatibilidade com as bibliotecas
atuais e melhorando a legibilidade do código.
A equipe atual tem pouco conhecimento sobre testes automatizados e estamos
implementando pytest.

[Statement]
Analise o trecho de código abaixo e refatore-o para Python 3, mantendo a lógica
de negócio, melhorando a legibilidade e adicionando testes unitários básicos
usando pytest.

[CÓDIGO]

[Personality]
Responda de forma didática e detalhada, explicando cada alteração feita no
código e sugerindo boas práticas modernas.

[Experiment]
Forneça duas abordagens alternativas de refatoração:
1. Uma abordagem mínima, apenas corrigindo compatibilidade.
2. Uma abordagem moderna, aplicando padrões atuais e sugerindo melhorias.
```

## RACE

Reúne **papel, ação, contexto e resultado esperado**. É útil quando você já
sabe o que precisa fazer e quer definir critérios claros para a entrega.

- **R — Role (papel):** diga qual perspectiva profissional usar.
- **A — Action (ação):** indique a tarefa a executar.
- **C — Context (contexto):** apresente o cenário e suas restrições.
- **E — Expectation (expectativa):** especifique o formato e os critérios da saída.

### Exemplo

```txt
[RACE]

[Role]
Você é um desenvolvedor sênior especializado em refatoração de código legado
em Java, com experiência em migração para padrões modernos e aplicação de
testes unitários.

[Action]
Reescreva a classe abaixo para torná-la compatível com Java 17, seguindo boas
práticas de programação orientada a objetos e adicionando testes unitários
com JUnit 5.

[Context]
O código foi escrito originalmente em Java 6 e utiliza APIs e convenções
desatualizadas.
Nosso objetivo é melhorar manutenibilidade, legibilidade e cobertura de testes,
sem alterar a lógica de negócio.

[CÓDIGO]

[Expectation]
Forneça:
1.A nova versão da classe com comentários explicando cada modificação.
2.Um arquivo de teste unitário separado.
3.A resposta em formato Markdown usando blocos de código para cada trecho
(código refatorado e testes).
```

## CO-STAR

Define **objetivo, apresentação e público** junto ao contexto. É útil quando
uma resposta técnica precisa seguir um formato e um tom específicos.

- **C — Context (contexto):** descreva a situação atual.
- **O — Objective (objetivo):** indique o resultado que deseja alcançar.
- **S — Style (estilo):** escolha a forma de apresentação.
- **T — Tone (tom):** defina a atitude da comunicação.
- **A — Audience (público):** diga para quem a resposta se destina.
- **R — Response (resposta):** especifique a estrutura da entrega.

### Exemplo

```txt
[CO-STAR]

[Context]
O projeto faz parte de um sistema bancário escrito em C# 5.0 há mais de 10 anos.
Precisamos modernizar a base para .NET 8, garantindo compatibilidade, segurança
e aplicando boas práticas de programação assíncrona.

[Objective]
Refatore o código legado a seguir para atualizar para .NET 8, melhorar a
legibilidade, aplicar async/await onde for apropriado e sugerir padrões modernos
de logging e tratamento de erros.

[CÓDIGO]

[Style]
Apresente as soluções em estilo técnico e organizado, com explicações curtas
logo após cada bloco de código.

[Tone]
Use um tom formal e instrutivo, adequado para documentação técnica de equipe
de desenvolvimento.

[Audience]
A resposta é destinada a desenvolvedores juniores e plenos que vão manter e
evoluir este código após a refatoração.

[Response]
Forneça:
1.O código refatorado usando blocos de código Markdown.
2.Comentários explicativos inline sobre cada modificação importante.
3.Um checklist resumindo as melhorias aplicadas (compatibilidade, async/await,
logging, tratamento de erros).
```
