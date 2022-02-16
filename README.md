# InstallAPKonWearOs

Este é um breve tutorial ensinando como install um APK no WearOs, neste tutorial estarei utilizando o moto360 (wear) e um computador com sistema operacional linux.

## Passo a Passo

1. Primeiro será necessário habilitar a função desenvolvedor no relogio para isso siga esses passos: 

Habilitar opção de desenvolvedor no relógio
No seu relógio vá em configurações -> sistema -> sobre. Agora ache o campo Número de Versão e clique 7x . Agora irá mostrar na tela do relógio que a opção de desenvolvedor foi habilitada 


2. Agora é necessário habilitar a depuração por Wi-fi:

No seu relógio vá em configurações -> opções do desenvolvedor. Agora habilite a opção depuração ADB ( irá aparecer um dialog perguntar se você realmente quer habilitar essa funcionalidade, aperte para confirmar)  e depois Habilite a depuração por WI-FI. Pode demorar alguns segundos e em baixo irá aparecer o endereço IP que você usará para se conectar ao relogio. O IP deve parecer algo como isto: 192.168.0.27:5555

<img width="302" alt="image" src="https://user-images.githubusercontent.com/38574345/154283512-609beab7-3edd-467e-833c-fe1201c192e9.png">

No meu caso o ip foi 192.168.0.108:5555

3. Agora **NO COMPUTADOR** digite o seguinte comando para conectar ao relogio: ``` adb connect <ip>``` no meu caso fica: 
 ``` adb connect 192.168.0.108:5555```

4. Ainda no computador, abra o terminal vá na pasta a onde você deixou o APK do relógio e digite o seguinte comando ``` adb -e install <nome do apk>``` no meu caso ficou da seguinte forma:   ```adb -e install wearable-staging.apk```

Se der tudo certo é para aparecer da seguinte forma:

<img width="710" alt="image" src="https://user-images.githubusercontent.com/38574345/154284675-fbdc0629-52a4-4f35-9503-a055ff9be454.png">

E agora ele irá aparecer na listas de App do relógio.
