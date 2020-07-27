# Recuperação de senha

**RF  requisitos funcionais**
- O usuário deve poder recuperar sua senha informando o seu e-mail;
- O usuário deve receber um e-mail com instruções de recuperação de senha;
- O usuário deve poder resetar sua senha;

**RFN Requsitos não funcionais**

- Utilizar Mailtrap para testar envios em ambiente de dev;
- Utilizar Amazon SES para envios em produção;
- O envio de e-mails deve acontecer em segunfo plano (background job);

**RN Regras de negocios**

- O link enviado port email para resetar senha, deve expirar em 2h;
- O usuário precisa confirmar a nova senha ao resetar sua senha;

# Atualização do Perfil

**RF  requisitos funcionais**

- O usuário deve poder atualizar seu nome, senha e-mail;

**RN Regras de negocios**

- O usuário não pode alterar seu email para um email já utilizado;
- Para atualizar sua senha o usuário deve informar a senha antiga;
- Para atualizar sua senha o usuário deve informar a senha nova;



# Painel do prestator

**RF  requisitos funcionais**
- O usuário deve poder listar seus agendamentos de um dia especifíco;
- O prestador deve receber uma notificação sempre que houver um novo agendamento;
- O prestador deve poder visualizar as notifícações não lidas;

**RFN Requsitos não funcionais**

- Os agendamentos do prestador no dia devem ser armazenados em cache;
- As notificações do prestador devem ser armazenadas no MongoDB;
- As notificações do prestador devem ser enviadas em tempo-real utilizando Socket.io;

**RN Regras de negocios**

- A notificação dever ter um status de lida ou não-lida para que o prestador possa controlar;


# Agendamento do serviços

**RF  requisitos funcionais**
- O usuário deve poder listar todos prestadores de serviços cadastrados;
- O usuário deve listar os dias de um mês com pelo menos um horário disponivel de um prestador;
- O usuário deve poder listar horários disponiveis em um dia especifico de um prestador;
- O usuário deve poder realizar um novo agendamento com um prestador;

**RFN Requsitos não funcionais**

- A listagem de prestadores deve ser armazenada em cache;

**RN Regras de negocios**

- Cada agendamento deve durar 1h exatamente;
- Os agendamentos devem estar disponíveis entre 8h ás 18h (primeiro ás 8h, último ás 18h);
- O usuário não pode agendar em um horário já ocupado;
- O usuário não pode agendar em um horário que já passou;
- O usuário não pode agendar serviços consigo mesmo;




