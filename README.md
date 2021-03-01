# Ambiente TypeScrypt

Projeto setado para trabalhar com Typescipt

## Instalação

Use o package manager [NPM](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm/) para instalar as dependencias.

```bash
npm i
```

## Exmeplo

```js
import express from 'express';
import cors from 'cors';
import logger from 'morgan';
import path from 'path';
import routes from './routes/index';

const app = express();

app.use(cors());
app.use(express.json());
app.use(express.urlencoded({ extended: false }));
app.disable('x-powered-by');
app.use(logger('combined'));
app.use('/api', routes);
app.use(
  '/api/uploads',
  express.static(path.resolve(__dirname, '..', 'uploads')),
);

export default app;

```

## Contributing
Estou sempre em busca de melhorias, caso veja algo que poderia ser diferente, me avise! =D

## License
[MIT](https://choosealicense.com/licenses/mit/)
