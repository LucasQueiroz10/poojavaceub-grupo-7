```mermaid
classDiagram
  class Produto {
  +preco: float
  +quantidade: int
  + mostrarValor(): float
}
  class Instrumento {
  - cor: string
  - tamanho: float
  - peso: float
  - marca: string
}
  class Acessório {
  - nome: string
  - cor: string
  - tamanho: string
  - peso: float
  - marca: string
  }
Produto <|-- Instrumento
Produto <|-- Acessório

  class Corda {
  - nome: string
  + produzirSom(): void
}
  class Metal {
  - nome: string
  + produzirSom(): void
}
  class Percussao {
  - nome: string
  + produzirSom(): void
}

Instrumento <|-- Corda
Instrumento <|-- Metal
Instrumento <|-- Percussao

```
