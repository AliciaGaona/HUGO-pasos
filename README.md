# HUGO pasos antes de

Versión para usar Chocolatey/Windows 10

1. Instalar Chocolatey:

  - Abrir la consola Power shell como administrador
  
  ![image](https://user-images.githubusercontent.com/99162884/183562740-5a8df3f1-3133-4df3-bec2-fdc3ca1baa42.png)

  ![image](https://user-images.githubusercontent.com/99162884/183562670-a96af9fc-cc00-408d-a0fc-9934276e4311.png)


  - Verificar los permisos con el siguiente comando:
  
    ![image](https://user-images.githubusercontent.com/99162884/183562869-efb23c0a-6cf5-4b82-ab34-c42c07752be2.png)

  - Si no hay permisos, habilitar permisos con el siguienet comando:
    
    ![image](https://user-images.githubusercontent.com/99162884/183562989-823062bd-4b2b-4094-92a4-73b456864fd4.png)
    
  - Utilizar comando para instalar Chocolatey, el paso a paso => [Pasos instalar Chocolatey](https://www.solvetic.com/tutoriales/article/8886-instalar-chocolatey-en-windows-10/)
  
  - Verificar versión de choco
    
    ![image](https://user-images.githubusercontent.com/99162884/183563441-02d20d16-adff-42b8-8da6-b47e18dda42d.png)

    

2. Instalar HUGO en tu PC, 
[instalar HUGO](https://gohugo.io/getting-started/installing/)

![image](https://user-images.githubusercontent.com/99162884/183563531-6036200e-d8d5-492d-a131-e879aacae2a1.png)


3. Elegir tema, es muy importante revisar que sea compatible con la versión de HUGO instalada [Temas Hugo](https://themes.gohugo.io), para acceder al tema le das click y aparecerán las carateristicas, para acceder el repo original dar click en botón download

![image](https://user-images.githubusercontent.com/99162884/183565145-f4f8efb4-b407-4fe2-bf1e-375c3fc7c5ee.png)

![image](https://user-images.githubusercontent.com/99162884/183565439-e2e331d0-c2d1-4218-89e1-063b80e67b7d.png)


4. Crear un Fork del tema elegido en tu repositorio de GitHub.[Link de tema elegido de HUGO](https://themes.gohugo.io/themes/hugo-theme-sam/)

![image](https://user-images.githubusercontent.com/99162884/183564961-18d88ec8-f3ed-4a5d-b183-82b253f7a9c1.png)

5. Crear un nuevo sitio HUGO por medio de la línea de comando (en mi caso uso directamente git bash) comando =>  `hugo new nombreDelSitio`
6. Subir el proyecto que te creo HUGO a tu repositorio de GitHub. Lo anterior se realiza versioanndo tu proyecto y enviando commit de todo tu proyecto.

![image](https://user-images.githubusercontent.com/99162884/183565655-a4cd244c-7402-4a35-9f9e-73f8e9356c24.png)

7. Hay que enlazar los repositorios por medio de submodulos de GitHub, en el rep que te creo HUGO crearemos un submódulo en una carpeta llamada themes, muy importante que la carpeta que gurade este submódulo tenga el mismo nombre de tu tema. en este caso la ruta seria algo asi  `themes/hugo-theme-sam`

`git add submodule git@github.com:AliciaGaona/hugo-theme-sam.git themes/hugo-theme-sam`

__git add submodule__-agregar nuevo submódulo
__git@github.com:AliciaGaona/hugo-theme-sam.git__ - url de GitHub del fork del tema(la url para clonar repositorio)
__themes/hugo-theme-sam__ - ruta donde se hará el submódulo

8. Realizar commit de nuevo submódulo, el resultado sería algo así:

![image](https://user-images.githubusercontent.com/99162884/183567253-bf10bdac-cf4f-475d-aed9-af0b41f836ed.png)

9. 





