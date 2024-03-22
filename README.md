<img src="https://oriondesign.art.br/wp-content/uploads/2023/08/Thumb-Typebot-copiar-4.png">

# Auto Instalador de Typebot

Este autoinstalador se probó utilizando un VPS Contabo vacío (4vCores + 8Gb Ram) con **Ubunto 20.04**
En esta versión, puedes elegir los puertos durante la instalación, lo que permite integrar Typebot con cualquier otra aplicación.

### 📌 Notas importantes:

Instalación realizada en Docker (si tiene otros contenedores, pueden fallar durante el proceso de instalación con este instalador automático;

Recomiendo crear una instantánea de su VPS para evitar cualquier problema que pueda ocurrir;

Antes de la instalación, es extremadamente importante que cree 3 registros en el DNS, a saber, “typebot”, “bot” y “storage”. Todos de Tipo **A**, todos apuntando a la **ip de tu VPS**, con **Proxy desactivado** y **TTL Auto** (o el valor que venga).
<details>
   <summary>Acerca del registro de Typebot</summary>
   <i>Es a través de este que podremos acceder al sistema para crear nuestro bot, también conocido como Builder</i><br><br>
   • Tipo: <b>A</b><br>
   • Entrada: <b>typebot</b><br>
   • Contenido: <b>IP del servidor</b><br><br>
   <img src="https://file.notion.so/f/s/c14b5ac1-d43a-4f18-bd76-4f10bd4262f1/Untitled.png?id=9855df72-743c-439d-b865-ec8391b93cc4&table=block&spaceId=f554c1aa-b56c -4ac0-88b1-4679371e6777&expirationTimestamp=1692072000000&signature=whfO8e8AETlGp2JEWdt0ML-i1QIlPr4kejWSGPXk-qY&downloadName=Untitled.png">
</details>
<details>
   <summary>Acerca del registro de bot</summary>
   <i>Esta es la pantalla Bot Viewer, por lo que cuando publiques tu bot, aparecerá a través del enlace bot.tudominio.com.br</i><br><br>
   • Tipo: <b>A</b><br>
   • Entrada: <b>bot</b><br>
   • Contenido: <b>IP del servidor</b><br><br>
   <img src="https://file.notion.so/f/s/236f6cc3-4857-4c48-a9d0-8b0b35c0ba94/Untitled.png?id=5703d967-1b89-423f-a6b1-60a377785be4&table=block&spaceId=f554c1aa-b56c -4ac0-88b1-4679371e6777&expirationTimestamp=1692072000000&signature=k1X9OIvmNeNfFzrKQg5xpqcS-HLcY9_x4zoc1sq8M6o&downloadName=Untitled.png">
</details>
<details>
   <summary>Acerca del registro de almacenamiento</summary>
   <i>Lo usamos para guardar imágenes, videos y audios en nuestro servidor, por lo que no necesita exportar su contenido a ningún otro lugar y usar el enlace en nuestro Typebot.</i><br><br>
   • Tipo: <b>A</b><br>
   • Entrada: <b>almacenamiento</b><br>
   • Contenido: <b>IP del servidor</b><br><br>
   <img src="https://file.notion.so/f/s/571842de-ad54-42e3-980e-542204b6ad0c/Untitled.png?id=c5772588-3c3f-4bd9-ad5c-8c7fc29d3d0a&table=block&spaceId=f554c1aa-b56c-4ac0-88b1-4679371e6777&expirationTimestamp=1692072000000&signature=OHFt_mSTmTRB9PEnhwllhnHQdCbzOa69ewqj5_PYRIc&downloadName=Untitled.png">
</details>

<hr/>

## 📀 Instalación de Typebot

1- Copia el siguiente comando y pégalo en tu terminal:
```
sudo apt install -y git && git clone https://github.com/elboga5/typebot.git && cd autoinstalltypebot && chmod +x typebot.sh && ./typebot.sh
```

Cuando ejecute este código, le pedirá que proporcione la siguiente información:
   - Enlace del constructor (por ejemplo, typebot.tudominio.com);
   - Puerto del constructor (predeterminado: 3001);
   - Enlace del visor (por ejemplo, view.tudominio.com);
   - Puerto del visor (predeterminado: 3002);
   - Enlace de almacenamiento (por ejemplo, storage.sudominio.com);
   - Puerto de almacenamiento (predeterminado: 9000);
   - Su correo electrónico (por ejemplo, contacto@dominio.com);
   - Contraseña de su correo electrónico (si es gmail, debe ser la contraseña de la aplicación);
   - SMTP desde su correo electrónico (ej: smtp.hostinger.com);
   - Puerto SMTP (ej: 465);
   - SMTP_SECURE (si el puerto SMTP es 465, escriba verdadero; de lo contrario, escriba falso);
   - Clave secreta de 32 caracteres (generada en el sitio web: <a href="https://codebeautify.org/generate-random-hexadecimal-numbers">codebeautify</a>).

Después de completar los campos correctamente, comenzará a instalar y configurar Typebot.

>
> Al final de la instalación aparecerá un mensaje, escriba "Y" y "ENTER" para completar la instalación de typebot.
>

<hr/>

<br><br><br>
Ahora quédate con el pato bailarín:<br><br>
<img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExM3hpaTI2dzVuMGZmMnFteWE1bW80Z29hYXZub3cybTQyZHFrc2VoaSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/b9QBHfcNpvqDK/giphy.gif">
