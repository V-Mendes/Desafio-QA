Documentação do Projeto

 . Plano de Fluxo de Trabalho (Ciclo de Vida do Bug)
 O ciclo de vida de um bug segue as seguintes etapas:
 • Reportar Bug
 • Triagem
 • Desenvolvimento
 • Teste
 • Deploy/Correção
 • Encerrado

 . User Stories
 US01 - Login: Como usuário cadastrado, quero acessar o sistema com meu e-mail e senha para
 ter acesso às minhas informações.
 US02 - Recuperar Senha: Como usuário esquecido, quero redefinir minha senha para conseguir
 acessar novamente minha conta.

 . Mind-map (US01 - Login)
 • Login
 • → Inputs: Email, Senha
 • → Validação: Campos obrigatórios, Formato do email
 • → Ações: Botão Entrar
 • → Erros: Email inválido, Senha incorreta, Conta bloqueada

  . Casos de Teste (Step-by-step)
 CT01 - Login válido
 1. Acessar página de login
 2. Inserir e-mail válido
 3. Inserir senha válida
 4. Clicar em 'Entrar'
 Resultado esperado: Acesso permitido ao sistema.
 ----------
 CT02 - Login inválido (senha incorreta)
 1. Acessar página de login
 2. Inserir e-mail válido
 3. Inserir senha incorreta
 4. Clicar em 'Entrar'
 Resultado esperado: Mensagem de erro 'Senha incorreta'.

 0. Casos de Teste (BDD)
 Feature: Login
 Scenario: Login com credenciais válidas
 Given que estou na tela de login
 When insiro um email válido e senha válida
 And clico no botão 'Entrar'
 Then devo acessar o sistema com sucesso
 ----------
 Feature: Login
 Scenario: Tentativa de login com senha incorreta
 Given que estou na tela de login
 When insiro um email válido e senha incorreta
 And clico no botão 'Entrar'
 Then devo ver a mensagem 'Senha incorreta
