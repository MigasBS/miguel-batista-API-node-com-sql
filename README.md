# Construção de API REST com Node.js e MySQL

**Disciplina:** Programação Web III (PW3)  
**Aluno:** Miguel Batista da Silva
**Turma:** PW3  

---

## Como Rodar o Projeto Localmente

### 1. Clonar o repositório
```bash
git clone https://github.com/SEU_USUARIO/miguel-batista-API-node-com-sql.git
cd miguel-batista-API-node-com-sql
```

### 2. Instalar dependências
```bash
npm install
```

### 3. Configurar variáveis de ambiente
Copie o arquivo `.env.example` para `.env` e ajuste as credenciais do seu banco de dados se necessário:
```bash
cp .env.example .env
```

### 4. Criar o Banco de Dados e a Tabela
Execute o script `schema.sql` no seu MySQL ou MariaDB:
```bash
mysql -u root -p < schema.sql
```
Ou abra o arquivo `schema.sql` e execute as instruções SQL no seu cliente de banco de dados (DBeaver, phpMyAdmin, MySQL Workbench ou terminal).

### 5. Iniciar o Servidor
Modo desenvolvimento com recarregamento automático:
```bash
npm run watch
```
O servidor estará rodando em: `http://localhost:3002`

---

## Rotas da API

| Método | Rota | Descrição |
|---|---|---|
| `POST` | `/usuarios` | Cadastra um novo usuário (`nome` e `email` no body) |
| `GET` | `/usuarios` | Lista todos os usuários cadastrados |
| `PUT` | `/usuarios/:id` | Atualiza dados do usuário informado no parâmetro de rota |
| `DELETE` | `/usuarios/:id` | Remove o usuário pelo ID |
