
<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Poppins&size=28&duration=3500&pause=900&color=2563EB&center=true&vCenter=true&width=820&lines=Prácticas+Intermedias;Arduino" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Secci%C3%B3n-D-10B981?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Semestre-2-F59E0B?style=for-the-badge" />
</p>

# Primeros pasos con arduino

## Instalación de Proteus con librerías de Arduino

### 1. Descargar arduino 8.13 

[Link de descarga](https://drive.google.com/file/d/1ouQSQnzWfMGr_i82AxI1g2FiqmFKyLRh/view?usp=sharing)

<div align="center">
  <img src="img/1.avif" alt="" width="80%">
</div>

### 2. Descomprimir el archivo

<div align="center">
  <img src="img/2.avif" alt="" width="80%">
</div>

### 3. Elegir la ruta donde se instalará proteus

<div align="center">
  <img src="img/3.avif" alt="" width="80%">
</div>

### 4. Iniciar la instalación de Proteus 8.13 SP0 Pro.exe

<div align="center">
  <img src="img/4.avif" alt="" width="80%">
</div>

### 5. Dar click en Finalizar. No abrir todavía.

<div align="center">
  <img src="img/5.avif" alt="" width="80%">
</div>

### 6. Copiar la carpeta "Data" y pegarla en la ruta donde se instaló proteus

<div align="center">
  <img src="img/6.avif" alt="" width="80%">
</div>

Si se eligió la ruta por default, entonces se tiene que pegar en:

```
C:\Program Files (x86)\Labcenter Electronics\Proteus 8 Professional
```

> Con esto se instalan las librerías parara trabajar con arduino.

### 7. Iniciar proteus y crear un nuevo proyecto

<div align="center">
  <img src="img/7.avif" alt="" width="80%">
</div>

### 8. Dejar por default todo y dar en siguiente

<div align="center">
  <img src="img/8.avif" alt="" width="80%">
</div>

<div align="center">
  <img src="img/9.avif" alt="" width="80%">
</div>

<div align="center">
  <img src="img/10.avif" alt="" width="80%">
</div>

<div align="center">
  <img src="img/11.avif" alt="" width="80%">
</div>

### 9. Ya creado el proyecto en la pestaña "Devices" dar click en "P" y apareceran los distintos tipos de arduinos al buscarlos

<div align="center">
  <img src="img/12.avif" alt="" width="80%">
</div>

### 10. Al seleccionarlo y hacer click en aceptar, aparecerá en la pantalla

<div align="center">
  <img src="img/13.avif" alt="" width="80%">
</div>


## Instalación de Arduino IDE

### 1. Ir a la [página oficial de arduino ide](https://docs.arduino.cc/software/ide/)

<div align="center">
  <img src="img/14.avif" alt="" width="80%">
</div>

### 2. Elegir el sistema operativo y descargar el instalador

<div align="center">
  <img src="img/15.avif" alt="" width="80%">
</div>

### 3. Abrir el archivo descargado e iniciar el instalador

<div align="center">
  <img src="img/16.avif" alt="" width="80%">
</div>

### 4. Elegir la ruta de instalación

<div align="center">
  <img src="img/17.avif" alt="" width="80%">
</div>

### 5. Finalizar instalación y abrir

<div align="center">
  <img src="img/18.avif" alt="" width="80%">
</div>

### 6. Instalar libería para la familia de Arduino

Ir a Tools > Board > Board

<div align="center">
  <img src="img/19.avif" alt="" width="80%">
</div>

Se desplegará un menú donde se deberá instalar la opción "Arduino AVR BOARDS by Arduino"

<div align="center">
  <img src="img/20.avif" alt="" width="80%">
</div>

<div align="center">
  <img src="img/21.avif" alt="" width="80%">
</div>

Si se instaló correctamente dirá "installed"

> Con esto ya se podrá trabajar ya las familias de arduino (nano, uno, mega...)

<div align="center">
  <img src="img/22.avif" alt="" width="80%">
</div>


## Simular programas arduino en proteus

Creamos el código que queremos simular, en este caso será un código para encender un led.

```
void setup() {
  pinMode(13, OUTPUT);
}

void loop() {
  digitalWrite(13, HIGH); // Enciende
  delay(1000);              // Espera 1 segundo
  digitalWrite(13, LOW);   // Apaga
  delay(1000);              // Espera 1 segundo
}
```

Elegímos arduino uno, se puede elegir cualquier otro pero debe de coincidir el tipo de Arduino tanto en "Arduino IDE" y "Proteus".

<div align="center">
  <img src="img/22.avif" alt="" width="80%">
</div>

### Dar click en el botón de "Verify" (botón en forma de check ✓) y se compilará el código

<div align="center">
  <img src="img/23.avif" alt="" width="80%">
</div>


### Se debe de obtener la ruta del código compilado

Se debe de marcar la siguiente opción:

> File > Preferences > Show verbose output during > compile (marcar ✓)

<div align="center">
  <img src="img/24.avif" alt="" width="80%">
</div>

Se vuelve a compilar y ahora saldrá la información de la compilación 

<div align="center">
  <img src="img/25.avif" alt="" width="80%">
</div>

Se debe hacer scroll hacia la derecha y se debe buscar y copiar la ruta que tenga extensión ".hex" sin comillas ejemplo:

> C:\\Users\\hugo1\\AppData\\Local\\arduino\\sketches\\B9CE229681D14CC9A18026035FECB803/sketch_sep25a.ino.hex

<div align="center">
  <img src="img/26.avif" alt="" width="80%">
</div>

### Copiar la ruta del compilado en proteus

Hace click sobre encima del arduino y se desplegará un menú con varias opciones.

<div align="center">
  <img src="img/27.avif" alt="" width="80%">
</div>

En la opción de "Program File" se debe de pegar la ruta que anteriormente se copió. Ya con esto al iniciar la simulación en proteus, se ejecutará el código.

<div align="center">
  <img src="img/28.avif" alt="" width="80%">
</div>

> Esto se debe de hacer solo una vez ya que la ruta siempre será la misma cada vez que se compile. A excepción que se cree otro proyecto, entonces habrá que actualizar la ruta.

<div align="center">
  <img src="img/29.avif" alt="" width="80%">
</div>

