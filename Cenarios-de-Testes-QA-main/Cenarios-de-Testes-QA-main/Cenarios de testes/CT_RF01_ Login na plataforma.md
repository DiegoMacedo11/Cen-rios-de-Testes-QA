## Cenário 01: Login na plataforma.

### Caso de Teste 01: Login com as credenciais válidas.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C01-CT01 | O login será realizado com um nome de usuário e uma senha válidos. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| As credenciais fornecidas (usuário e senha) devem ser válidas. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login do OrangeHRM              |
| **E** preenchemos "Admin" no campo usuário                        |
| **E** preenchemos "admin123" no campo senha                       |
| **QUANDO** clicarmos no botão "Login"                             |
| **ENTÃO** seremos redirecionados para o Dashboard do sistema      |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O redirecionamento para o Dashboard deve ocorrer corretamente.  |

---

### Caso de Teste 02: Tentativa de login com senha incorreta.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C01-CT02 | O login falhará quando a senha for inválida.             |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário \"Admin\" deve existir no sistema. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login do OrangeHRM              |
| **E** preenchemos "Admin" no campo usuário                        |
| **E** preenchemos "senhaerrada" no campo senha                    |
| **QUANDO** clicarmos no botão "Login"                             |
| **ENTÃO** uma mensagem de erro \"Invalid credentials\" será exibida |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A mensagem de erro \"Invalid credentials\" deve ser exibida.    |

---

### Caso de Teste 03: Tentativa de login com campos em branco.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C01-CT03 | O login falhará quando os campos obrigatórios estiverem em branco. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Nenhuma. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login do OrangeHRM              |
| **E** deixamos os campos de usuário e senha em branco             |
| **QUANDO** clicarmos no botão "Login"                             |
| **ENTÃO** deve ser exibida a mensagem \"Required\" em ambos os campos |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Os campos obrigatórios devem exibir mensagens de validação.     |

## 🔗 Evidências (Jam.dev)

- **C01-CT01** → [Execução](https://jam.dev/c/5bbbe6ae-5b5e-46ac-b44f-55a315f35278)  
- **C01-CT02** → [Execução](https://jam.dev/c/4892394e-02a2-4efb-a1fb-9db8f9aa85f2)  
- **C01-CT03** → [Execução](https://jam.dev/c/e68df062-59fb-4dc1-8b79-4a6b16dee0c1) 


