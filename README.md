# Embajadoras Cloud - Aplicación Full-Stack con AWS Amplify

## Modelo de Datos

Crea tu modelo de datos en la consola de Amplify:

![Data Model](https://raw.githubusercontent.com/anacunha/amplify-embajadoras-cloud/main/content/DataModel.png)

## Contenido

| Name              | Description                                     | Photo                                                                                                     | Type   |
| ----------------- | ----------------------------------------------- | --------------------------------------------------------------------------------------------------------- | ------ |
| Athena            | Compañera fiel                                  | https://raw.githubusercontent.com/anacunha/amplify-embajadoras-cloud/main/content/pets/Athena.jpg         | DOG    |
| Chuby             | También conocido como Chewbacca                 | https://raw.githubusercontent.com/anacunha/amplify-embajadoras-cloud/main/content/pets/Chuby.jpg          | DOG    |
| Gremlina          | Llamada así en honor a los Gremlins 🐈‍⬛          | https://raw.githubusercontent.com/anacunha/amplify-embajadoras-cloud/main/content/pets/Gremlina.png       | CAT    |
| Lambeau & Fortuna | Los perros de Memo 🖤                           | https://raw.githubusercontent.com/anacunha/amplify-embajadoras-cloud/main/content/pets/LambeauFortuna.jpg | DOG    |
| Tatá              | Jabuti de 13 años 🐢                            | https://raw.githubusercontent.com/anacunha/amplify-embajadoras-cloud/main/content/pets/Tata.jpg           | TURTLE |
| Tempestade        | Adorable pero nadie puede domarla 🌪            | https://raw.githubusercontent.com/anacunha/amplify-embajadoras-cloud/main/content/pets/Tempestade.jpg     | CAT    |

## UI Library

## Configuración de la Aplicación

Crea una aplicación React:

```shell
npx create-react-app@latest adopta-una-mascota
cd adopta-una-mascota
```

Instala la CLI de Amplify:

```shell
npm install -g @aws-amplify/cli
```

Instala las dependencias de npm:

```shell
npm install aws-amplify @aws-amplify/ui-react
```

Configure Amplify agregando el siguiente código en su archivo index.js:

```javascript
import { ThemeProvider } from "@aws-amplify/ui-react";
import { Amplify } from 'aws-amplify';

import awsconfig from './aws-exports';

import "@aws-amplify/ui-react/styles.css";
import { studioTheme } from "./ui-components";

Amplify.configure(awsconfig);
```

En App.js, envuelva el componente `<App>` en `<ThemeProvider>`:

```javascript
<ThemeProvider theme={studioTheme}>
  <App/>
</ThemeProvider>
```

## Uso del Componente

Haz `amplify pull` los componentes más recientes:

```shell
amplify pull
```

En App.js, importa y utiliza el componente:

```javscript
import './App.css';
import { Flex } from "@aws-amplify/ui-react";
import {PetCardCollection} from './ui-components';

function App() {
  return (
    <div className="App">
      <Flex justifyContent="center">
        <PetCardCollection />
      </Flex>
    </div>
  );
}

export default App;
```
