```mermaid
classDiagram
  class Fornecedor {
    - nome: string
    - cnpj: string
    - contato: string
    - endereco: string

    +cadastrarProduto(produto: Produto): void
    +listarProdutos(): string
    +getNome(): string
    +atualizarContato(novoContato: string): void
  }

  class Produto {
    - nome: string
    - preco: float
  }



Fornecedor "1" o-- "*" Produto : fornece
