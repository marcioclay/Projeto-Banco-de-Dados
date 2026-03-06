# Exercício de Modelagem Conceitual de Banco de Dados

## Objetivo
Neste exercício o aluno deverá:

1. Definir o **Mini Mundo**
2. Criar o **Dicionário de Dados**
3. Construir o **Modelo Conceitual (Entidades e Relacionamentos)**

---

# Parte 1 — Mini Mundo

O **Mini Mundo** descreve o contexto do sistema que será modelado.  
Deve conter uma explicação clara do problema e das informações que precisam ser armazenadas.

## Descrição do Mini Mundo

(Escreva aqui a descrição do sistema)

Exemplo de perguntas para ajudar:

- Qual é o sistema?
- Quem utiliza o sistema?
- Quais informações precisam ser armazenadas?
- Existe relacionamento entre os dados?

---

# Parte 2 — Dicionário de Dados

O **Dicionário de Dados** descreve os dados que existirão no banco.

Cada entidade deve listar seus atributos.

## Modelo de tabela

| Entidade | Atributo | Descrição |
|--------|--------|--------|
| | | |
| | | |
| | | |

---

# Parte 3 — Modelo Conceitual

O **Modelo Conceitual** representa:

- Entidades
- Atributos
- Relacionamentos

Normalmente é representado usando **Diagrama Entidade-Relacionamento (DER)**.

## Entidades identificadas

Liste as entidades do sistema.

Exemplo:

- Entidade 1:
- Entidade 2:
- Entidade 3:

## Relacionamentos

Descreva como as entidades se relacionam.

Exemplo:
Aluno --- realiza --- Matrícula
Curso --- possui --- Matrícula


---

# Exemplo Completo ( Esta parte é um MODELO)

## Mini Mundo

Uma escola deseja informatizar o controle de seus cursos.

A escola possui **alunos** e **cursos**.  
Cada aluno pode se matricular em um ou mais cursos.  
Cada curso possui um professor responsável.

O sistema deve armazenar:

- dados dos alunos
- dados dos cursos
- informações de matrícula
- professores responsáveis pelos cursos

---

## Dicionário de Dados

| Entidade | Atributo | Descrição |
|--------|--------|--------|
| Aluno | id_aluno | Identificador do aluno |
| Aluno | nome | Nome do aluno |
| Aluno | email | Email do aluno |
| Curso | id_curso | Identificador do curso |
| Curso | nome_curso | Nome do curso |
| Curso | carga_horaria | Carga horária |
| Professor | id_professor | Identificador do professor |
| Professor | nome | Nome do professor |
| Matrícula | data_matricula | Data da matrícula |

---

## Modelo Conceitual

### Entidades

Aluno  
Curso  
Professor  
Matrícula

### Relacionamentos
Aluno --- realiza --- Matrícula

Curso --- possui --- Matrícula

Professor --- ministra --- Curso 


### Descrição

- Um **Aluno** pode realizar várias **Matrículas**
- Um **Curso** pode possuir várias **Matrículas**
- Um **Professor** pode ministrar vários **Cursos**

---

# Atividade

Crie um modelo conceitual para o seguinte sistema:

Sistema: _______________________________________

1. Descreva o Mini Mundo
2. Monte o Dicionário de Dados
3. Identifique Entidades
4. Defina os Relacionamentos
5. Desenhe o DER
