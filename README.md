# Hackintosh OpenCore 0.71 MSI Bazooka B450m MAX WiFi

Configuración de OpenCore 0.71 con soporte para macOS BigSur (11.4). 

Todo funciona :) (ok, facetime no)

Novedades: 

* Puertos USB configurados para esta tarjeta.
* Parches AMD actualizados.
* Controlador de WiFi nativo sin soporte de AirDrop.
* OpenRGB compilado para esta motherboard, no ofrece control total de RGB, pero es algo.

## Conjunto de hardware

* Tarjeta madre: MSI Bazooka B450m MAX WiFi 

* Versión BIOS: 7C87v16 (2021-05-25)
* CPU: AMD Ryzen 3600x 
* GPU: Sapphire Pulse Rx580 8GB
* RAM: 32 GB
* Almacenamiento: Crucial MX500 AHCI SATA
* Monitor 4K + Monitor secundario 1080p

## Preparación

1. Upgrade/Downgrade BIOS, si se tiene instalada una versión más reciente es posible que OpenCore no consiga iniciar el instalador o el SO. Las versiones 7C87v10, 7C87v11, 7C87v12, 7C87v14 y 7C87v16 funcionan correctamente.
2. Configurar BIOS
   - Almacenamiento en modo AHCI
   - Boot en modo CSM -> UEFI MODE falla con mi GPU pero puedes intentarlo.
   - Deshabilitar Above 4g memory/cryptocurrency mining.

## Instalación

Cree un medio de instalación, en mi caso he tenido éxito siguiento el método de Recovery de macOS Catalina ->  https://youtu.be/khs7kEAELWc Gracias a Brandon Yen.

O crea un medio de instalación USB desde macOS https://support.apple.com/es-co/HT201372

## Post-Instalación

Una vez instalado, es necesario cambiar el número de serie -> https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html

AMD Power Gadget para vigilar la temperatura y rendimiento del CPU y OpenRGB para disfrutar de tus luces RGB.

## Créditos

* Dortiana OpenCore https://dortania.github.io/OpenCore-Install-Guide/
* Soporte WiFi y Bluetooth https://github.com/OpenIntelWireless 
* AMD Power Optimization https://github.com/trulyspinach
* OpenRGB https://gitlab.com/CalcProgrammer1/OpenRGB

