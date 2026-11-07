## Role prompting

O role prompting **consiste em dar um "Role" (um cargo) para o modelo de IA
generativa** antes de começar a o prompting, Essa técnica estimula o reciocionio
especializado, utilizando padrões de raciocinio da área especificada.

### Exemplo

```txt
Aja como um desenvolvedor de software sênior com ampla experiência em Java
```

## Chain of Thought

Consiste em **instruir o modelo a prosseguir passo a passo apresentando todas as
etapas envolvidas**, para isso deve-se utilizar exemplos de como queremos a saída

### Exemplo

```txt
Você é um engenheiro de software experiente e sempre explica seu passo a passo
antes de dar uma resposta final

Vamos resolver um problema sobre tempos de deployment.

Qual pipeline de deployment é mais rápido?
Opção 1:
Etapa de build de 15min, testes unitários 20min, testes de integração 25min e
deploy para a produção leva 10 min

Opção 2:
Etapa de build de 12min, testes unitários 25min, testes de integração 20min e
deploy para a produção leva 15 min

*** Raciocínio passo a passo***
Opção 1: 15 + 20 + 25 + 10 = 70 min
Opção 2: 12 + 25 + 20 + 15 = 72 min

Como 70 min é menor que 72min, opção 1 é mais rápida

---

Agora tente este:

Qual pipeline é mais rápido?:

Opção 1: Etapa de build de 30min, testes unitários 40min, testes de integração
15min e deploy para a produção leva 20 min

Opção 2: Etapa de build de 25min, testes unitários 30min, testes de integração
25min e deploy para a produção leva 30 min

```

## In Context Learning

Consiste em **ensinar no próprio prompt como executar uma tarefa a partir de
exemplos**, o In Context Learning está ligado aos conceitos de **Shot base
prompting**, que são prompts orientados por exemplo, dentre eles temos, **Zero
Shot prompting**, **One Shot Prompting**, **Few Shot prompting** e etc...

### Exemplo

```txt
Traduza as frases para JSON no formato {"en":"", "pt": ""}

Entrada: "Hello"
Saída: {"en": "Hello", "pt":"Olá"}
Entrada: "Good Morning"
Saída: ...
```
## Meta Prompting

Consiste em **pedir para a própria IA revisar o prompt para identificar**
**qualquer ambiguidade ou inconsistencia**, mas isso deve ser usado como uma forma
de **"debuggar"** o prompt, não deve ser uma solução preguiçosa para fazer prompts 
mais rápido, caso você tenha uma suspeita de que o promblema é o prompt use o meta 
prompting para reavalia-lo e reconstrui-lo

### Exemplo

```txt
Revise meu ultimo prompt e idenfique qualquer ambiguidade ou informação ausente. Como
posso reescreve-lo para ser mais conciso e preciso?
```

Obs: Parece que é o cachorro correndo atrás do próprio rabo mas por incrível que pareça
funciona!.

## Prompt Embutido

Consiste em **incluir uma instrução fixa dentro de uma aplicação ou fluxo de
trabalho**, para que ela seja enviada à IA junto com o pedido do usuário. Assim,
o modelo recebe orientações sobre como responder, mesmo quando o usuário não
escreve essas instruções a cada interação.

### Exemplo

```txt
Instrução embutida no aplicativo:
Você é um assistente de suporte técnico. Responda em português e dê passos
curtos e objetivos para resolver o problema.

Pedido do usuário:
Meu computador não se conecta ao Wi-Fi. O que posso fazer?
```
