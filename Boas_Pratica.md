# Módulo 6 — Relacionamentos, Integridade e Boas Práticas

## 🎯 Objetivos
Garantir a integridade dos dados e aplicar boas práticas de modelagem.

## 🧠 Conceitos

### Integridade de Dados
- **Entidade:** cada registro identificado unicamente (PK).
- **Referencial:** vínculos entre tabelas devem ser válidos (FK).
- **Domínio:** tipo e valor permitido (ex: idade >= 0).
- **Integridade de negócio:** regras que valem para a aplicação (ex.: saldo não negativo).

### Tipos de Relacionamento
- 1:1 — Um aluno possui um prontuário.
- 1:N — Um curso possui vários alunos.
- N:N — Alunos e cursos (com tabela intermediária).

### Boas Práticas
- Nomeie colunas com clareza (`id_aluno`, não apenas `id`).
- Use singular para nomes de tabela (Aluno, Curso).
- Prefira chaves numéricas simples (inteiros, auto incremento).
- Documente relacionamentos e regras de negócio.
- Valide no SGBD e na aplicação (defesa em profundidade).

## 🧱 Exemplo Final (consulta com JOIN)
\`\`\`sql
SELECT a.nome AS Aluno, c.nome AS Curso
FROM Aluno a
JOIN Matricula m ON a.id_aluno = m.id_aluno
JOIN Curso c ON m.id_curso = c.id_curso;
\`\`\`

## ✅ Checklist para entrega/avaliação
- MER completo e legível.
- Modelo lógico com PKs e FKs definidos.
- Tabelas implementadas (DDL) com tipos e restrições.
- Exemplos de consultas (SELECT, JOIN, agregações).
- Justificativas de normalização/denormalização.
