# Módulo 2 — Modelo Conceitual (MER)

## 🎯 Objetivos
Compreender e aplicar o Modelo Entidade-Relacionamento (MER) para representar o mundo real.

## 🧠 Conceitos

### Entidades
Representam **objetos do mundo real** que possuem existência própria.
Exemplo: Aluno, Curso, Professor.

### Atributos
Características que descrevem as entidades.
Exemplo: nome, matrícula, CPF, data_nascimento.

### Chave Primária
Atributo que **identifica unicamente** cada registro.
Exemplo: `id_aluno`.

### Relacionamentos
Indicam **como as entidades se relacionam** entre si.
Tipos:
- 1:1 — Um para Um  
- 1:N — Um para Muitos  
- N:N — Muitos para Muitos

### Cardinalidade
Define a quantidade de ocorrências entre as entidades.

## 🧱 Exemplo Prático

**Entidades:**
- Aluno(id_aluno, nome, cpf)
- Curso(id_curso, nome, carga_horaria)

**Relacionamento:**
Aluno **matricula-se** em Curso  
Tipo: N:N (um aluno pode cursar vários cursos, e um curso pode ter vários alunos)

## 📊 Diagrama MER (Descrição)
```
[Aluno]---< Matricula >---[Curso]
```
## 💡 Dica
No caso de relacionamentos N:N, cria-se uma **entidade associativa** (ex: Matricula).
