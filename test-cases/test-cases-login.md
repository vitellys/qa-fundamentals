## Caso de Teste – Login na Área de Game

**Autora:** Ellen Rebeca Simões de Albuquerque  
**Cargo-alvo:** QA Júnior  

### Objetivo
Validar o funcionamento do login na área de game, garantindo que o jogador consiga acessar sua conta com segurança e que informações importantes como progresso, itens e ranking sejam carregadas corretamente após a autenticação.

---

### Contexto
A plataforma possui uma área restrita para jogadores cadastrados, onde ficam disponíveis dados de perfil, progresso salvo, conquistas e ranking. Qualquer falha no login pode impactar diretamente a experiência do usuário e gerar perda de confiança no sistema.

---

### Cenário 1 – Login realizado com sucesso

**Pré-condição:** Jogador cadastrado e com progresso salvo anteriormente.

**Passos:**
1. Acessar a tela de login da plataforma
2. Informar e-mail válido
3. Informar senha válida
4. Clicar no botão “Entrar”

**Resultado esperado:**
- Login realizado com sucesso
- Perfil do jogador carregado corretamente
- Progresso salvo recuperado sem inconsistências
- Itens e conquistas exibidos corretamente
- Ranking apresentado conforme último estado salvo

---

### Cenário 2 – Tentativa de login com senha inválida

**Passos:**
1. Acessar a tela de login
2. Informar e-mail válido
3. Informar senha inválida
4. Clicar em “Entrar”

**Resultado esperado:**
- Sistema impede o acesso
- Mensagem de erro clara e compreensível para o jogador
- Nenhuma informação sensível é exposta

---

### Cenário 3 – Falha de conexão durante o login

**Passos:**
1. Iniciar login com credenciais válidas
2. Simular queda de conexão durante o carregamento

**Resultado esperado:**
- Sistema informa falha de conexão
- Jogador não perde progresso salvo anteriormente
- Opção de tentar novamente é apresentada
- Não ocorre duplicação de sessão

---

### Observação
Durante os testes, é importante validar não apenas se o login funciona, mas se o usuário entende o que está acontecendo. Em sistemas de game, a preservação do progresso e a clareza das mensagens são fatores essenciais para a experiência do jogador.
