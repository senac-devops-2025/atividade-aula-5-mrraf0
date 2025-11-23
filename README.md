[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=21794216)
# Aula 05 – Shift Security Left / SCA / Proteção de Credenciais

Este repositório é o **template** da atividade da Aula 05. Você (aluno) deve:
1. Clonar o *repo* criado automaticamente pelo GitHub Classroom a partir deste template.
2. Executar os testes localmente (`pytest`).
3. Comitar e *push* do código.
4. Ver o *pipeline* de CI rodar (build + testes + verificação de segredos com Gitleaks).
5. Conferir os alertas do **Dependabot** (SCA) quando existirem.
6. Abrir um PR com uma correção simples (ex.: atualizar versão de dependência) e validar o CI novamente.

> Importante: **NÃO** suba segredos. Use arquivos `.env.example` e variáveis de ambiente locais. O pipeline contém uma verificação de segredos (Gitleaks).

## Passos rápidos (aluno)
- Criar e ativar venv:
  ```bash
  python -m venv .venv
  source .venv/bin/activate  # Windows: .venv\Scripts\activate
  python -m pip install --upgrade pip
  pip install -r requirements.txt
  pip install -r requirements-dev.txt
  pytest -q
  ```
- Rodar a aplicação local (exemplo):
  ```bash
  python app/main.py
  ```

## O que entregar
- Pipeline de CI passando (build + testes).
- Um artefato de build publicado pela pipeline (`app-dist.zip`).
- (Opcional, recomendado) Um PR do Dependabot aceito atualizando uma dependência.

## Estrutura
- `app/` – código da aplicação.
- `tests/` – testes automatizados (pytest).
- `.github/workflows/ci.yml` – pipeline CI (build + teste + gitleaks + artefato).
- `.github/dependabot.yml` – configuração SCA (dependências `pip` e `github-actions`).
- `SECURITY.md` – práticas de credenciais e como habilitar secret scanning/push protection.
- `CLASSROOM/instrucoes_aluno.md` – guia detalhado para você.
- `CLASSROOM/instrucoes_professor.md` – guia para o professor configurar a tarefa no Classroom.
