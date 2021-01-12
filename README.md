# Links
- https://docs.google.com/presentation/d/1MhqVH0ieg8ILsQVTY-HJFzuDFyIHiTF2zmPu9QZbmxU/edit

# Bibliotecas
- Styled Components
- Styled JSX

## Styled Components

- Vantagens
  - Critical CSS automático
  - Escopo definido(sem colisão de classes)
  - Remoção de CSS não utilizado
  - Estilos dinâmicos(props, themes)
  - Manutenção simplificada
  - Vendor prefixing automático(-moz-)

### Exemplos

#### Estilo estático
```js
import styled from 'styled-components'

export const Main = styled.div`
  align-items: center;
  display: center;
`
```

#### Estilo dinâmico
```js
import styled from 'styled-components'

const Button = styled.button`
  background-color: ${props.primary ? '#0f0' : '#fff'};
`

render (
  <div>
    <Button>btn1</Button>
    <Button primary>btn2</Button>
  </div>
)
```


#### Estilo estendido
```js
import styled from 'styled-components'

const Button = styled.button`
  color: #FFF;
  font-size: 1rem;
  padding: 1em;
`

const TomatoButton = styled(Button)`
 color: tomato;
` 
render (
  <div>
    <Button>btn1</Button>
    <TomatoButton primary>btn2</TomatoButton>
  </div>
)
```
