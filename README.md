# Tarefaemsqlusandojob
-- Criação da tabela de tarefas para PostgreSQL
CREATE TABLE Tarefas (
    ID SERIAL PRIMARY KEY,
    Nome VARCHAR(255) NOT NULL,
    Descricao TEXT,
    DataCriacao DATE NOT NULL,
    DataConclusao DATE,
    Concluida BOOLEAN DEFAULT FALSE
);

-- Exemplo de inserção de tarefa usando uma job (PostgreSQL não tem uma funcionalidade de job built-in)
INSERT INTO Tarefas (Nome, Descricao, DataCriacao)
VALUES ('Completar o projeto', 'Terminar o projeto de exemplo em SQL', CURRENT_DATE);
