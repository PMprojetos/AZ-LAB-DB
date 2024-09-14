# Laboratório de Exploração: Configuração de Banco de Dados no Azure

Este README descreve os passos básicos para configurar uma instância de banco de dados na Azure, focando em exploração inicial usando o **Azure Hub**.

## Pré-requisitos

Antes de começar, certifique-se de que você possui:

- Uma **conta ativa** no Azure.
- Um **grupo de recursos** já configurado.
- **Permissões adequadas** para criar e gerenciar serviços no Azure.

## Passos para Configurar o Banco de Dados

### 1. Criar um Banco de Dados SQL

1. Acesse o [Portal do Azure](https://portal.azure.com).
2. No painel, clique em **Criar um recurso** e selecione **Banco de Dados SQL**.
3. Preencha as informações:
   - **Nome do banco de dados**: Escolha um nome para seu banco.
   - **Servidor**: Crie um novo servidor ou selecione um existente.
   - **Grupo de recursos**: Utilize um grupo já existente ou crie um novo.
   - **Camada de serviço**: Escolha uma opção de camada básica para testes.

### 2. Configurar Acesso ao Banco

1. Vá até as configurações do **servidor SQL** e clique em **Regras de firewall**.
2. Adicione o IP público da sua máquina local para permitir conexões.
3. Salve as alterações.

### 3. Conectar-se ao Banco de Dados

Conecte-se ao banco de dados usando uma ferramenta como o **Azure Data Studio** ou via **CLI** com o seguinte comando:

```bash
sqlcmd -S <servidor>.database.windows.net -d <nome-do-banco> -U <usuário> -P <senha>
```

### 4. Explorar e Testar o Banco de Dados

Agora, você pode começar a explorar e rodar consultas SQL simples para testar a conectividade e funcionalidade do banco de dados.

## Limpar Recursos (Opcional)

Após finalizar a exploração, você pode remover os recursos para evitar cobranças adicionais:

```bash
az group delete --name <nome-do-grupo>
```

---

Esse laboratório foi desenvolvido para fins de exploração inicial no Azure Hub.
