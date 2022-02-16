# InstallAPKonWearOs

Este é um breve tutorial ensinando como install um APK no WearOs, neste tutorial estarei utilizando o moto360 (wear) e um computador com sistema operacional linux.

## Passo a Passo

1. Primeiro será necessário habilitar a função desenvolvedor no relogio para isso siga esses passos: 

Enable Developer Options
On your Android Wear watch you'll need to go into Settings, System, About, find the Build Number and tap this seven times. You'll now see a new option in the Settings menu called Developer Options.

2. Agora é necessário habilitar a depuração por Wi-fi:

In the Developer Options menu look for and enable an option called ADB debugging, and confirm that you wish to do so when asked. Below this you should also see Debug over Wi-Fi. Enable this, give it a moment to connect, then jot down the IP address that appears below. It will look something like 192.168.0.27:5555

<img width="302" alt="image" src="https://user-images.githubusercontent.com/38574345/154283512-609beab7-3edd-467e-833c-fe1201c192e9.png">

No meu caso o ip foi 192.168.0.108:5555

3. Agora **NO COMPUTADOR** digite o seguinte comando para conectar ao relogio: ``` adb connect <ip>``` no meu caso fica: 
 ``` adb connect 192.168.0.108:5555```

4. Ainda no computador, abra o terminal vá na pasta a onde você deixou o APK do relógio e digite o seguinte comando ``` adb -e install <nome do apk>``` no meu caso ficou da seguinte forma:   ```adb -e install wearable-staging.apk```

Se der tudo certo é para aparecer da seguinte forma:

<img width="710" alt="image" src="https://user-images.githubusercontent.com/38574345/154284675-fbdc0629-52a4-4f35-9503-a055ff9be454.png">

E agora ele irá aparecer na listas de App do relógio.
