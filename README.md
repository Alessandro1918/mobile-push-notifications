# mobile-push-notifications

## 🚀 Projeto
Um projeto minimalista mostrando o funcionamento de envio de notificações para aplicativos de celular usando a plataforma Expo

<div align="center">
    <img src="github/demo.jpg" alt="demo" title="demo" width="50%"/>
</div>

## 🛠️ Tecnologias
- [Expo](https://expo.dev)

## 🗂️ Utilização

### 🐑🐑 Clonando o repositório:

```bash
  $ git clone url-do-projeto.git
```

### ▶️ Rodando o App:

#### <img alt="icon" width="35px" src="https://github.com/dhanishgajjar/terminal-icons/raw/master/png/dracula.png"/> No terminal:
```bash
  $ cd mobile-push-notifications
  $ npm install             #download dependencies to node_modules
  $ npx expo start          #start the project
```

#### <img alt="icon" width="35px" src="https://cdn-icons-png.flaticon.com/512/2482/2482985.png"/> No celular:
- Conectar o celular na mesma rede wi-fi do computador;
- Abrir o app [Expo Go](https://play.google.com/store/apps/details?id=host.exp.exponent);
- Clicar no botão "Scan QR Code" para escanear o QR code do terminal;
- Aguardar o Expo compilar o código do projeto e rodar a aplicação no celular;
- Ao iniciar, o app vai exibir o Expo Push Token desse dispositivo. Copiar esse token (ex: <code>ExponentPushToken[4dGCABC...]</code>);

#### <img alt="icon" width="35px" src="https://cdn-icons-png.flaticon.com/512/2933/2933245.png"/> No computador:
- Usar o Postman / Insomnia para enviar a seguinte requisição HTTP:
```bash
  POST https://exp.host/--/api/v2/push/send
  Body:
  {
    "to": "ExponentPushToken[4dGCABC...]",  //use your token here
    "title": "Hello World!",
    "body": "Directly from my Expo App!",
    "data": {
      "userID": 42,                         //any custom key-value pair
      "coins": 123,                         //of data to be used
      "event": "specialSale1234"            //by the app
    }
  }
```

### 📋 TODO:
- Customizar ícone da notificação ([veja mais](https://docs.expo.dev/versions/latest/sdk/notifications/#credentials))
- Implantar em ambiente de Produção ([veja mais](https://docs.expo.dev/push-notifications/faq/#notifications-work-in-development-but-not-after-building-the-app))
