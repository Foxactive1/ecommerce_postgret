# Ecommerce Supabase

Esta é uma aplicação web de ecommerce construída utilizando [Supabase](https://supabase.com/) como backend. O projeto demonstra como criar uma interface completa de loja virtual com autenticação, gerenciamento de produtos, carrinho de compras, pedidos, perfil do usuário e painel administrativo.

## Funcionalidades

- **Catálogo de Produtos:** Lista produtos cadastrados com imagens, preços e opção de compra.
- **Carrinho de Compras:** Adicione produtos, altere quantidade, remova itens e finalize pedidos. O carrinho é persistido no `localStorage`.
- **Pedidos:** Usuários autenticados podem visualizar seus pedidos, ver detalhes e status.
- **Perfil do Usuário:** Gerencie informações de conta como nome, email e telefone.
- **Autenticação:** Cadastro e login via Supabase Auth, com feedback de erro/sucesso. Logout disponível.
- **Administração:** Usuário administrador (por email) tem acesso a painel administrativo para visualizar estatísticas, gerenciar produtos e ver receita total.
- **Estatísticas:** Cards com dados de produtos, categorias, pedidos e clientes.
- **Responsividade:** Layout adaptável para dispositivos móveis.
- **Mensagens:** Feedback visual para ações importantes (sucesso/erro).

## Tecnologias Utilizadas

- **Frontend:** HTML, CSS, JavaScript (Vanilla)
- **Backend:** Supabase (Auth, Database)
- **Bibliotecas:** [@supabase/supabase-js](https://github.com/supabase/supabase-js) via CDN

## Estrutura das Principais Tabelas (Supabase)

- **products:** Produtos da loja
- **categories:** Categorias dos produtos
- **orders:** Pedidos realizados
- **order_items:** Itens dos pedidos
- **customers:** Dados dos clientes

## Como Executar

1. **Clone o projeto**

2. **Configure seu Supabase**
   - Crie um novo projeto no Supabase.
   - Crie as tabelas: `products`, `categories`, `orders`, `order_items`, `customers`.
   - Ajuste permissões conforme necessário.

3. **Configure as credenciais**
   - Substitua as variáveis `SUPABASE_URL` e `SUPABASE_ANON_KEY` no início do `<script>`.

4. **Abra o arquivo HTML**
   - Basta abrir o arquivo `index.html` em seu navegador.

## Painel Administrativo

- O painel admin é visível apenas para o email cadastrado como administrador (default: `innovaideia@gmail.com`).
- Permite visualizar estatísticas, receita, gerenciar produtos (adicionar, editar, excluir).

## Observações

- Adição/Edição/Exclusão de produtos via painel admin precisam ser implementadas em modal ou página dedicada.
- Para produção, nunca exponha chaves sensíveis ou use ANON_KEY para operações administrativas.
- O fluxo de autenticação, feedback e persistência são apenas exemplos e podem ser melhorados para produção.

## Telas

- Home com estatísticas
- Catálogo de produtos
- Carrinho de compras
- Pedidos do usuário
- Perfil do usuário
- Painel administrativo (admin)

## Licença

Este projeto é apenas para fins educacionais/demonstração.

---

### Exemplo de configuração Supabase

```js
const SUPABASE_URL = 'https://<your-project>.supabase.co';
const SUPABASE_ANON_KEY = '<your-anon-key>';
const supabase = window.supabase.createClient(SUPABASE_URL, SUPABASE_ANON_KEY);
```

---

### Contato

Para dúvidas ou sugestões, abra uma issue ou envie email para o autor.
