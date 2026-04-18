![Banner Atlantis](img/bannerAtlantis.png)

# Atlantis CLI

O Atlantis é um sistema de gestão para parques aquáticos, clubes e hotéis. Nesta versão, o projeto atende ao MVP solicitado na atividade com um CLI em TypeScript para cadastro e gerenciamento de clientes titulares e dependentes.

## Funcionalidades implementadas

- CRUD de clientes em memória
- Cadastro de clientes dependentes vinculados a um titular
- Listagem de dependentes de um titular específico
- Listagem do titular de um dependente específico
- Carga inicial de dados para facilitar demonstração e testes
- Execução compatível com CI sem bloquear em entrada interativa

## Padrões e organização

- `Singleton`: a classe `Armazem` concentra os clientes durante a execução
- `Strategy`: o menu principal delega as ações para processos específicos
- `Prototype`: `Endereco` e `Telefone` continuam com suporte a clonagem

## Como executar

```bash
npm install
npm run build
npm start
```

## Menu principal

Ao iniciar em modo interativo, o sistema oferece as opções:

- cadastrar cliente titular
- cadastrar cliente dependente
- listar clientes
- atualizar cliente
- remover cliente
- listar dependentes por titular
- listar titular por dependente

## Observação sobre CI

Quando a variável `CI=true` estiver definida, o sistema não abre prompts. Em vez disso, ele carrega os dados iniciais e imprime um resumo dos clientes cadastrados.
