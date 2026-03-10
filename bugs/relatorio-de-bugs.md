# Relatório de Bugs — Desafio QA Beedoo 2026

Este documento apresenta os bugs identificados durante a execução dos casos de teste do módulo de cadastro e listagem de cursos.

---

## BUG 01 — Cadastro de curso permite nome vazio (CT02)

**Caso de Teste Relacionado:** CT02 — Validação de campo obrigatório (Nome do curso)

**Severidade:** Média

**Descrição:**  
O sistema permite realizar o cadastro de um curso mesmo quando o campo "Nome do curso" não é preenchido.

**Passos para reproduzir:**
1. Acessar a tela de cadastro de cursos.
2. Preencher todos os campos obrigatórios exceto o nome do curso.
3. Clicar em "Cadastrar curso".

**Resultado Atual:**  
O curso é cadastrado normalmente mesmo com o campo nome vazio.

**Resultado Esperado:**  
O sistema deve impedir o cadastro e exibir mensagem informando que o nome do curso é obrigatório.

**Evidência:**  
Disponível na pasta CT02-falhou no link abaixo
https://drive.google.com/drive/folders/1ZslnXsFCjUta_N5icoRMKj_Upmdvsb9l?usp=sharing


---

## BUG 02 — Sistema permite datas inválidas no cadastro (CT03)

**Caso de Teste Relacionado:** CT03 — Validação de datas do curso

**Severidade:** Média

**Descrição:**  
O sistema permite cadastrar cursos onde a data final é anterior à data inicial, gerando inconsistência lógica nas informações.

**Passos para reproduzir:**
1. Acessar o cadastro de cursos.
2. Preencher os campos obrigatórios.
3. Inserir uma data inicial posterior à data final.
4. Clicar em "Cadastrar curso".

**Resultado Atual:**  
O curso é cadastrado normalmente com datas inválidas.

**Resultado Esperado:**  
O sistema deve validar as datas e impedir o cadastro quando a data final for anterior à data inicial.

**Evidência:**  
Disponível na pasta CT03-falhou no link abaixo
https://drive.google.com/drive/folders/1ZslnXsFCjUta_N5icoRMKj_Upmdvsb9l?usp=sharing

---

## BUG 03 — Sistema aceita número negativo de vagas (CT04)

**Caso de Teste Relacionado:** CT04 — Validação do campo número de vagas

**Severidade:** Média

**Descrição:**  
O campo "Número de vagas" aceita valores negativos, permitindo o cadastro de cursos com informações inconsistentes.

**Passos para reproduzir:**
1. Acessar o cadastro de cursos.
2. Preencher os campos obrigatórios.
3. Inserir um valor negativo no campo número de vagas.
4. Clicar em "Cadastrar curso".

**Resultado Atual:**  
O curso é cadastrado com número negativo de vagas.

**Resultado Esperado:**  
O sistema deve aceitar apenas valores positivos e exibir mensagem de validação.

**Evidência:**  
Disponível na pasta CT04-falhou no link abaixo
https://drive.google.com/drive/folders/1ZslnXsFCjUta_N5icoRMKj_Upmdvsb9l?usp=sharing

---

## BUG 04 — Curso não é removido após exclusão (CT06)

**Caso de Teste Relacionado:** CT06 — Exclusão de curso

**Severidade:** Alta

**Descrição:**  
Ao excluir um curso, o sistema exibe mensagem de sucesso informando que o curso foi removido, porém o item permanece visível na listagem.

**Passos para reproduzir:**
1. Acessar a listagem de cursos.
2. Selecionar um curso existente.
3. Clicar no botão "Excluir".
4. Observar o comportamento da aplicação.
5. Atualizar a página.

**Resultado Atual:**  
Mensagem de exclusão exibida, porém o curso continua presente na listagem.

**Resultado Esperado:**  
O curso deve ser removido imediatamente e não deve reaparecer após atualização da página.

**Evidência:**  
Disponível na pasta CT06-falhou no link abaixo
https://drive.google.com/drive/folders/1ZslnXsFCjUta_N5icoRMKj_Upmdvsb9l?usp=sharing

---

## BUG 05 — Não é possível visualizar detalhes do curso (CT07)

**Caso de Teste Relacionado:** CT07 — Visualização de detalhes do curso

**Severidade:** Baixa

**Descrição:**  
Não existe funcionalidade disponível para visualizar os detalhes completos do curso, impedindo o acesso ao endereço (curso presencial) ou link de inscrição (curso online).

**Passos para reproduzir:**
1. Acessar a listagem de cursos.
2. Tentar clicar em um curso cadastrado.
3. Verificar se há opção de visualizar detalhes.

**Resultado Atual:**  
Nenhuma ação ocorre e não há tela ou modal de detalhes do curso.

**Resultado Esperado:**  
O sistema deveria permitir visualizar informações completas do curso.

**Evidência:**  
Disponível na pasta CT07-falhou no link abaixo
https://drive.google.com/drive/folders/1ZslnXsFCjUta_N5icoRMKj_Upmdvsb9l?usp=sharing

---
