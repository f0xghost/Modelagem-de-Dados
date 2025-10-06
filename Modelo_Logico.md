# Módulo 3 — Modelo Lógico (Relacional)

## 🎯 Objetivos
Converter o modelo conceitual (MER) em um modelo lógico relacional.

## 🧠 Conceitos

### Tabelas
Cada **entidade** vira uma **tabela**.
Cada **atributo** vira uma **coluna**.

### Chaves
- **Primária (PK):** identifica o registro.
- **Estrangeira (FK):** cria vínculo com outra tabela.

### Relacionamentos no Modelo Relacional
- 1:1 → FK em uma das tabelas
- 1:N → FK no lado N
- N:N → nova tabela intermediária

## 🧱 Exemplo Prático

### Entidades:
- Aluno(id_aluno PK, nome, cpf)
- Curso(id_curso PK, nome)
- Matricula(id_aluno FK, id_curso FK, data_matricula)

### Representação SQL

```sql
CREATE TABLE Aluno (
  id_aluno INT PRIMARY KEY,
  nome VARCHAR(100),
  cpf CHAR(11)
);

CREATE TABLE Curso (
  id_curso INT PRIMARY KEY,
  nome VARCHAR(100)
);

CREATE TABLE Matricula (
  id_aluno INT,
  id_curso INT,
  data_matricula DATE,
  PRIMARY KEY (id_aluno, id_curso),
  FOREIGN KEY (id_aluno) REFERENCES Aluno(id_aluno),
  FOREIGN KEY (id_curso) REFERENCES Curso(id_curso)
);
