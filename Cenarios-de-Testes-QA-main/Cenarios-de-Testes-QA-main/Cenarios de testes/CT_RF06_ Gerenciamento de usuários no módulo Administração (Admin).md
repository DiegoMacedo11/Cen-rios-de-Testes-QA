## Cenário 06: Gerenciamento de usuários no módulo Administração (Admin).

### Caso de Teste 01: Adicionar um novo usuário com dados válidos.

| ID       | Descrição                                                            |
| :------- | :------------------------------------------------------------------- |
| C06-CT01 | O sistema deve permitir o cadastro de um novo usuário com informações válidas. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado com permissões de administrador.  |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o administrador acessa o menu \"Admin\"             |
| **E** clica em \"Add\"                                           |
| **E** preenche os campos obrigatórios como \"Employee Name\", \"Username\" e \"Password\" |
| **QUANDO** clicar em \"Save\"                                    |
| **ENTÃO** o novo usuário deve ser cadastrado e listado corretamente |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O usuário cadastrado deve aparecer na lista de usuários ativos. |

---

### Caso de Teste 02: Tentativa de adicionar usuário com nome de usuário já existente.

| ID       | Descrição                                                                       |
| :------- | :------------------------------------------------------------------------------- |
| C06-CT02 | O sistema deve impedir o cadastro de um novo usuário com nome de usuário duplicado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Já deve existir um usuário com o mesmo nome de usuário.       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o administrador acessa o menu \"Admin\"             |
| **E** clica em \"Add\"                                           |
| **E** insere um nome de usuário que já existe                   |
| **QUANDO** clicar em \"Save\"                                    |
| **ENTÃO** uma mensagem de erro \"Already exists\" deve ser exibida |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve impedir o cadastro e exibir mensagem de duplicidade. |

---

### Caso de Teste 03: Filtrar usuários por status "Enabled".

| ID       | Descrição                                                      |
| :------- | :------------------------------------------------------------- |
| C06-CT03 | O sistema deve exibir apenas usuários com status "Enabled" ao aplicar o filtro. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Deve haver usuários com diferentes status (Enabled e Disabled). |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o administrador acessa o menu \"Admin\"             |
| **E** seleciona \"Enabled\" no campo \"Status\"                 |
| **QUANDO** clicar em \"Search\"                                  |
| **ENTÃO** apenas usuários com status \"Enabled\" devem ser exibidos na lista |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A lista deve conter apenas usuários com status "Enabled".       |

## 🔗 Evidências (Jam.dev)

- **C01-CT01** → [Execução](https://jam.dev/c/1d32163e-a298-4f4c-8c88-28a4565a5ffd)  
- **C01-CT02** → [Execução](https://jam.dev/c/263f4895-2d3b-4e51-991a-cd8cf6a18daf)  
- **C01-CT03** → [Execução](https://jam.dev/c/c845a434-5175-4596-9215-6579857eff8d)  
