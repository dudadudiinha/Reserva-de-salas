# Reserva de Salas
## Modelo Conceitual
### Descrição das Classes
#### Usuário:
- ##### Descrição: 
Representa qualquer pessoa que interage com o sistema, podendo ter diferentes perfis (Cliente, Administrador, etc.).

- ##### Atributos Principais: 
nome, email, senha, tipo.

- ##### Relacionamentos: 
Um usuário pode solicitar múltiplas reservas e avaliar múltiplas reservas.

#### Sala:
- ##### Descrição: 
Representa um espaço físico que pode ser reservado. Contém todas as informações sobre suas características e recursos.

- ##### Atributos Principais: 
id_sala, nome, capacidade, descricao, recursos.

- ##### Relacionamentos: 
Uma sala está associada a múltiplos espaços de tempo que podem ser reservados.

#### Reserva:
- ##### Descrição:
Entidade central que armazena os detalhes de um agendamento feito por um usuário para uma sala específica.

- ##### Atributos Principais: 
id_reserva, data_h_inicio, data_h_fim, status.

- ##### Relacionamentos: 
Uma reserva é solicitada por um Usuario , está associada a um Espaco (horário) específico e é analisada por um Avaliador.

#### Espaço:
- ##### Descrição: 
Representa um bloco de tempo disponível para uma determinada sala. Funciona como uma entidade associativa que conecta Sala e Reserva.

- ##### Atributos Principais: 
id_espaco.

- ##### Relacionamentos: 
Um espaço pertence a uma única Sala e pode estar vinculado a múltiplas Reservas (em caso de histórico).

#### Avaliador:
##### Descrição: 
Representa o usuário com permissão para aprovar ou recusar uma solicitação de reserva.

##### Atributos Principais: 
id_avaliador.

##### Relacionamentos: 
Um avaliador está associado a uma ou mais Reservas para realizar a avaliação da solicitação.
