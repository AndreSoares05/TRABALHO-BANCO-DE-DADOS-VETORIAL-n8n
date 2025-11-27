1 Recomendador de Receitas Fitness
n8n + Supabase + pgvector + OpenAI

Este projeto implementa um sistema inteligente de recomendação de receitas fitness utilizando embeddings, banco vetorial e automação com n8n.
A busca é semântica, permitindo ao usuário pedir receitas mesmo sem mencionar o nome exato.

2 Funcionalidade

O usuário envia mensagens como:

“quero algo com banana”

“me indique uma receita fitness”

“quero uma refeição rápida”

O sistema responde automaticamente com receitas relacionadas, usando:

✔ Embeddings
✔ Banco Vetorial (pgvector no Supabase)
✔ Workflow automatizado no n8n
✔ LLM para formatação da resposta

3 Tecnologias Utilizadas

Supabase (PostgreSQL + pgvector)

OpenAI Embeddings

OpenAI GPT

n8n Workflow Automation

SQL

4  Estrutura do Banco de Dados
CREATE TABLE receitas (
    id SERIAL PRIMARY KEY,
    titulo VARCHAR(150) NOT NULL,
    descricao TEXT,
    ingredientes TEXT NOT NULL,
    modo_preparo TEXT NOT NULL,
    tempo_preparo INT,
    rendimento VARCHAR(50),
    categoria VARCHAR(50),
    dificuldade VARCHAR(20),
    criado_em TIMESTAMP DEFAULT NOW()
);


A tabela foi populada com 10 receitas, incluindo Panqueca de Banana, Frango Fitness, Omelete, Salada Caesar, entre outras.

5 Arquitetura da Solução

Fluxo completo:

Mensagem do usuário → Embedding → Busca Vetorial → Receita Similar → GPT formata → Resposta final

6 Prints do Workflow (n8n)




7 Como Executar

Criar banco Supabase

Ativar extensão pgvector

Criar a tabela receitas

Inserir os dados

Importar workflow no n8n

Configurar chaves da OpenAI e Supabase

Enviar mensagens para o chatbot

8 Resultado

Recomendação automática de receitas

Busca baseada em significado

Respostas rápidas, completas e bem formatadas

Totalmente automatizado via n8n

9 Vídeo da Demonstração

📌 Adicionar aqui quando gravar:
[LINK DO VÍDEO]

👨‍💻 Autor

Nome:Marcos Andre dos Santos Soares
Disciplina: Projeto de Banco de Dados
Professor: Anderson Soares
