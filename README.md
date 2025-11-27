🥗 Recomendador de Receitas Fitness
n8n + Supabase + pgvector + OpenAI

Este projeto implementa um sistema inteligente de recomendação de receitas fitness utilizando embeddings, banco vetorial e automação com n8n.
A busca é semântica, permitindo ao usuário pedir receitas mesmo sem mencionar o nome exato.

📌 Funcionalidade

O usuário envia mensagens como:

“quero algo com banana”

“me indique uma receita fitness”

“quero uma refeição rápida”

O sistema responde automaticamente com receitas relacionadas, usando:

✔ Embeddings
✔ Banco Vetorial (pgvector no Supabase)
✔ Workflow automatizado no n8n
✔ LLM para formatação da resposta

🛠️ Tecnologias Utilizadas

Supabase (PostgreSQL + pgvector)

OpenAI Embeddings

OpenAI GPT

n8n Workflow Automation

SQL

🧬 Estrutura do Banco de Dados
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

⚙️ Arquitetura da Solução

Fluxo completo:

Mensagem do usuário → Embedding → Busca Vetorial → Receita Similar → GPT formata → Resposta final

🖥️ Prints do Workflow (n8n)
<img width="1273" height="596" alt="Screenshot 2025-11-27 145833" src="https://github.com/user-attachments/assets/514b2841-483b-4515-b95e-82a556a24e60" />
<img width="1365" height="719" alt="Screenshot 2025-11-27 154039" src="https://github.com/user-attachments/assets/176135fb-5b36-4f54-a484-444b3778be4c" />
<img width="1362" height="624" alt="Screenshot 2025-11-27 151331" src="https://github.com/user-attachments/assets/3d863ab7-39fb-4f27-be4e-7911dcac35ca" />
<img width="1349" height="477" alt="Screenshot 2025-11-27 151208" src="https://github.com/user-attachments/assets/577cce12-67ce-491c-98ea-5c37d68a0d74" />




▶️ Como Executar

Criar banco Supabase

Ativar extensão pgvector

Criar a tabela receitas

Inserir os dados

Importar workflow no n8n

Configurar chaves da OpenAI e Supabase

Enviar mensagens para o chatbot

📈 Resultado

Recomendação automática de receitas

Busca baseada em significado

Respostas rápidas, completas e bem formatadas

Totalmente automatizado via n8n

🎥 Vídeo da Demonstração

📌 Adicionar aqui quando gravar:
[https://youtu.be/UpdEkpfWcEk]

👨‍💻 Autor

Marcos Andre dos Santos Soares
Disciplina: Projeto de Banco de Dados
Professor: Anderson Soares
