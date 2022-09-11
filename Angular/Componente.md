# Componente

Um componente em angular é um *"pedaço"* da aplicação que representa um componente visual da sua tela. Esse componente contém um arquivo **.HTML**, **.TS** e um arquivo **.CSS**. Exemplo:

- home.component.html
- home.component.css
- home.component.ts

Podemos utilizar tudo em apenas um arquivo, porém, o recomentando é utilizar o formato dos 3 arquivos.

Quando criamos um componente, é gerado uma tag personalizada, que, por exemplo, seria ```<app-home></app-home>``` e dessa forma podemos referenciar todo o código **html**, toda a estilização do **css** e toda a lógica do **ts**. Ou seja, o componente encapsula as 3 tecnologias nessa tag.


```typescript
import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-home',
  templateUrl: './home.component.html',
  styleUrls: ['./home.component.css']
})

export class HomeComponent implements OnInit {
  constructor() {}

  ngOnInit(): void {

  }
}
```