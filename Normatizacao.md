# Módulo 4 — Normalização e Formas Normais

## 🎯 Objetivos
Entender e aplicar as Formas Normais para eliminar redundâncias e anomalias nos dados.

## 🧠 Conceitos

### O que é Normalização?
É o processo de **organizar os dados** em tabelas de forma eficiente, evitando:
- Repetições
- Inconsistências
- Anomalias de inserção, atualização e remoção

### 1FN — Primeira Forma Normal
- Todos os atributos são **atômicos** (sem listas ou campos compostos).
- Exemplo:
  - ❌ endereço = “Rua A, 123 - Bairro B”
  - ✅ rua = “Rua A”, numero = 123, bairro = “Bairro B”

### 2FN — Segunda Forma Normal
- Deve estar na 1FN.
- Nenhum atributo depende de **parte da chave primária** (importante quando existem chaves compostas).

### 3FN — Terceira Forma Normal
- Deve estar na 2FN.
- Nenhum atributo depende de **outro atributo não chave** (ou seja, sem dependências transitivas).

## 🧱 Exemplo Prático

Antes (ruim):
```
Aluno(id_aluno, nome, id_curso, nome_curso)
```

Problema: `nome_curso` depende de `id_curso`, não de `id_aluno` → violação da 3FN.

Depois (normalizado):
```
Aluno(id_aluno, nome, id_curso)
Curso(id_curso, nome_curso)
```

## 💡 Dicas
- Use normalização até o nível necessário: em sistemas analíticos (data warehouses) às vezes denormaliza por performance.
- Sempre documente as decisões de normalização.
