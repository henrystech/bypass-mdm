# Bypass-MDM for MacOS 26 Tahoe 💻

![mdm-screen](https://raw.githubusercontent.com/henrystech/bypass-mdm/main/mdm-screen.png)

#### Requisitos previos ⚠️

- **Se recomienda borrar el disco duro antes de comenzar.**
- **Se recomienda reinstalar macOS usando una memoria USB externa.**
- **El idioma del dispositivo debe configurarse en inglés; puede cambiarse después.**


#### Siga los pasos a continuación para omitir la configuración de MDM durante una instalación limpia de macOS.

> Al llegar a la etapa de configuración de inscripción MDM forzada:

1. Mantenga presionado el botón de encendido para apagar forzosamente su Mac.

2. Mantenga presionado el botón de encendido para iniciar su Mac y arrancar en modo de recuperación.

> a. **Mac con Apple Silicon**: mantenga presionado el botón de encendido.\
> b. **Mac con procesador Intel**: mantenga presionadas las teclas <kbd>CMD</kbd> + <kbd>R</kbd> durante el arranque.

3. Conéctese a Wi-Fi para activar su Mac.

4. Entre en el modo de recuperación y abra Safari.

5. Navegue a https://www.github.com/henrystech/bypass-mdm

6. Copie el script a continuación:
```zsh
curl https://raw.githubusercontent.com/henrystech/bypass-mdm/main/bypass-mdm.sh -o bypass-mdm.sh && chmod +x ./bypass-mdm.sh && ./bypass-mdm.sh
```

7. Abra Terminal (Utilidades > Terminal)

8. Pegue (<kbd>CMD</kbd> + <kbd>V</kbd>) y ejecute el script (<kbd>ENTER</kbd>).

9. Introduzca 1 para Autobypass.

10. Presione Enter para dejar el nombre de usuario predeterminado “Apple”.

11. Presione Enter para dejar la contraseña predeterminada “9876”.

12. Espere a que el script finalice y reinicie su Mac.

13. Inicie sesión con el usuario (Apple) y la contraseña (9876).

14. Omita toda la configuración (Apple ID, Siri, Touch ID, Servicios de ubicación).

15. Una vez en el escritorio, vaya a Configuración del sistema > Usuarios y grupos y cree su cuenta de Administrador real.

16. Cierre sesión del perfil Apple e inicie sesión con su perfil real.

17. Ahora puede configurar todo correctamente (Apple ID, Siri, Touch ID, Servicios de ubicación).

18. Una vez en el escritorio, vaya a Configuración del sistema > Usuarios y grupos y elimine el perfil Apple.

19. ¡Felicidades, está libre de MDM! 💫

###### Aunque es prácticamente imposible que detecten que has eliminado el MDM (porque ni siquiera llegó a configurarse), ten en cuenta que el número de serie del portátil seguirá apareciendo en el sistema de inventario de tu empresa. Estamos eliminando las capacidades del MDM antes de que se configure localmente, por lo que no estará disponible para ellos como un portátil administrado. Úsalo con precaución. Probablemente también sea buena idea tener una excusa válida.