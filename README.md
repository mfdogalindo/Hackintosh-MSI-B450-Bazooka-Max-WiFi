# Hackintosh OpenCore 0.66 MSI Bazooka B450m MAX WiFi

Configuración de OpenCore 0.66 con soporte para macOS Catalina (10.16.7) y BigSur (11.2). 

Todo funciona :)

## Conjunto de hardware

* Tarjeta madre: MSI Bazooka B450m MAX WiFi 

* Versión BIOS: 7C87v12 (2020-12-07)
* CPU: AMD Ryzen 3600x 
* GPU: Sapphire Pulse Rx580 8GB
* RAM: 32 GB
* Almacenamiento: Crucial MX500 AHCI SATA
* Monitor 4K + Monitor secundario 1080p

## Preparación

1. Upgrade/Downgrade BIOS, si se tiene instalada una versión más reciente es posible que OpenCore no consiga iniciar el instalador o el SO. Las versiones 7C87v10, 7C87v11 y 7C87v12 funcionan correctamente.
2. Configurar BIOS
   - Almacenamiento en modo AHCI
   - Boot en modo UEFI
   - Deshabilitar Above 4g memory/cryptocurrency mining.

## Instalación

Cree un medio de instalación, en mi caso he tenido éxito siguiento el método de Recovery de macOS Catalina ->  https://youtu.be/khs7kEAELWc Gracias a Brandon Yen.

Esta instalación se puede hacer desde WiFi configurando la conexión de red en el Kext *itlwm.kext/Contents/Info.plist*

Reemplace la línea *yourpwd* por la contraseña de la red y *yourssid* por el nombre de la red

```                xml
<key>WiFi_1</key>
<dict>
  <key>password</key>
  <string>yourpwd</string>
  <key>ssid</key>
  <string>yourssid</string>
</dict>
```

## Post-Instalación

Una vez instalado, es necesario cambiar el número de serie -> https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html

Instale HeliPort para conectar redes a WiFi y AMD Power Gadget para vigilar la temperatura y rendimiento del CPU.

## Créditos

* Dortiana OpenCore https://dortania.github.io/OpenCore-Install-Guide/
* Soporte WiFi y Bluetooth https://github.com/OpenIntelWireless 
* AMD Power Optimization https://github.com/trulyspinach

