classDiagram
  class Venda {
    - data: Date
    - valorFinal: float
    + gerarNotaFiscal(): string
    + getValorFinal(): float
  }

  class Funcionario {
    - cargo: string
    + registrarVenda(p: Pedido): Venda
    + getCargo(): string
  }

  class Pedido {
    - numero: int
    - listaProdutos: List<Produto>
    + adicionarProduto(p: Produto): void
    + calcularTotal(): float
  }

  Funcionario "1" --> "*" Venda : registra
  Pedido "1" --> "1" Venda : gera
