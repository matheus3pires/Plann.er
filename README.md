# Plann.er
Plann.er é uma aplicação desenvolvida para auxiliar usuários na organização de viagens, seja para lazer ou trabalho. Com o Plann.er, você pode criar e gerenciar suas viagens, adicionar atividades e links importantes, e gerenciar a confirmação de participantes.

## Funcionalidades
### Cadastro de Viagem
- Crie uma viagem informando o local de destino, datas de início e término, e-mails dos convidados, nome completo e endereço de e-mail do criador.
- Após criar uma viagem, o criador receberá um e-mail para confirmar a viagem. Após a confirmação, os convidados também receberão e-mails e o criador será redirecionado para a página da viagem.

### Confirmação de Participantes
- Os convidados devem confirmar sua presença clicando em um link recebido por e-mail e preencher seu nome para confirmar a participação.

### Gerenciamento da Viagem
- Adicione links importantes e atividades planejadas para a viagem na página dedicada.
- É possível convidar novos participantes e gerenciar confirmações diretamente na aplicação.

## Tecnologias Utilizadas
- Spring Boot: Framework principal para o desenvolvimento da aplicação.
- Flyway: Gerenciamento de migrações de banco de dados.
- DevTools: Ferramenta para facilitar o desenvolvimento.
- Lombok: Redução de boilerplate code.
- JPA: Mapeamento objeto-relacional.
- H2 Database: Banco de dados em memória para desenvolvimento e testes.

## Estrutura do Projeto
### Banco de Dados
- Tabela trips: Armazena informações sobre as viagens.
- Tabela participants: Armazena informações sobre os participantes.
- Tabela activities: Armazena atividades relacionadas à viagem.
- Tabela links: Armazena links importantes da viagem.

### Endpoints
#### Viagens
- Cadastro de Viagem
  - POST /trips
- Consulta de Viagem
  - GET /trips/{tripId}
- Atualização de Viagem
  - PUT /trips/{tripId}
- Confirmação de Viagem
  - GET /trips/{tripId}/confirm
- Convidar Participante
  - POST /trips/{tripId}/invites
- Consultar Participantes
  - GET /trips/{tripId}/participants
#### Participantes
- Confirmação de Participante
  - POST /participants/{participantId}/confirm
#### Atividades
- Cadastro de Atividade
  - POST /trips/{tripId}/activities
- Consultar Atividades
  - GET /trips/{tripId}/activities
#### Links
- Criação de Link
  - POST /trips/{tripId}/links
- Consultar Links
  - GET /trips/{tripId}/links

## Configuração e Execução
### Configuração do Banco de Dados
- A aplicação utiliza o H2 Database para desenvolvimento e testes. A configuração é feita automaticamente pelo Flyway com base nas migrações SQL.

### Execução da Aplicação
- Use o comando mvn spring-boot:run para iniciar a aplicação.

### Acesso à Aplicação
- Acesse a aplicação localmente em http://localhost:8080.

## Minhas Redes
Fique conectado para mais novidades e atualizações. Não hesite em entrar em contato!

- Linkedin: [linkedin.com/in/matheuspiress](https://www.linkedin.com/in/matheuspiress/)
- e-mail: matheuspiressdev@gmail.com
