# Estrutura das Branches

## Branch principal

**main**
Branch principal, sempre estável e pronta para entrega final do projeto.

---

## Branches de Sprint

**sprint-<numero>**
Branch que representa o ciclo de desenvolvimento de uma sprint.

Exemplos:

* `sprint-1`
* `sprint-2`
* `sprint-3`

**Regras:**

* Criada a partir da `main` no início da sprint.
* Serve como base para todas as features da sprint.
* Recebe o merge de todas as entregas da sprint.
* Ao final da sprint, deve ser mergeada na `main`.

---

## Branches de Desenvolvimento (filhas da sprint)

**feat/<nome-da-feature>**
Novas funcionalidades.

**bugfix/<nome-do-fix>**
Correções de bugs.

**hotfix/<nome-do-hotfix>**
Correções urgentes.

**refactor/<nome>**
Refatorações sem alteração de regra de negócio.

---

## Hierarquia de Branches

```
main
 └── sprint-2
      ├── feat/cadastro-aluno
      ├── feat/listagem-feedback
      ├── bugfix/erro-login
      └── refactor/service-layer
```

---

## Regras Gerais

* Nunca commitar diretamente na `main`.
* Nunca commitar diretamente na `sprint`.
* Toda branch de desenvolvimento deve ser criada a partir da branch da sprint atual.
* Nome das branches deve ser claro, objetivo, sem espaços e sem acentos.

---

## Fluxo de Trabalho

### 1. Início da Sprint

* Criar a branch da sprint:

```bash
git checkout main
git pull
git checkout -b sprint-2
git push -u origin sprint-2
```

---

### 2. Desenvolvimento

Para cada tarefa:

```bash
git checkout sprint-2
git pull
git checkout -b feat/nome-da-feature
```

---

### 3. Finalização da Feature

* Abrir Pull Request:

```
feat/* → sprint-2
```

---

### 4. Final da Sprint

* Após todas as features aprovadas:

```
sprint-2 → main
```

---

## Prazo para Último Commit e PR

* O último commit da feature deve ocorrer no máximo até **2 dias antes do fechamento da sprint**.
* O Pull Request deve ser aberto imediatamente após a finalização.
* No último dia da sprint, a branch `sprint-X` deve estar:

  * [ ] Estável
  * [ ] Revisada
  * [ ] Pronta para merge na `main`

---

## Processo de Pull Request

* O PR deve conter descrição objetiva do que foi feito.
* Deve informar quais tarefas do backlog estão sendo atendidas.
* Deve indicar possíveis impactos ou pontos de atenção.

### Tipos de PR

* `feat/* → sprint-X`
* `bugfix/* → sprint-X`
* `hotfix/* → sprint-X`
* `refactor/* → sprint-X`
* `sprint-X → main`

---

## Checklist obrigatório antes de abrir um PR

* [ ] Código revisado
* [ ] Testes executados
* [ ] Build funcionando
* [ ] Documentação atualizada
* [ ] Nome da branch está no padrão definido
* [ ] Base atualizada com a `sprint-X`
