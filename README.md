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
    
  - Utilizar comando para instalar Chocolatey, el paso a paso => [Pasos instalar Chocolatey](https://gohugo.io/getting-started/installing/)
  
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

5. Crear un nuevo sitio HUGO por medio de la línea de comando (en mi caso uso directamente git bash) comando =>  `hugo new site nombreDelSitio`
6. Subir el proyecto que te creo HUGO a tu repositorio de GitHub. Lo anterior se realiza versioanndo tu proyecto y enviando commit de todo tu proyecto.

![image](https://user-images.githubusercontent.com/99162884/183565655-a4cd244c-7402-4a35-9f9e-73f8e9356c24.png)

7. Hay que enlazar los repositorios por medio de submodulos de GitHub, en el rep que te creo HUGO crearemos un submódulo en una carpeta llamada themes, muy importante que la carpeta que gurade este submódulo tenga el mismo nombre de tu tema. en este caso la ruta seria algo asi  `themes/hugo-theme-sam`

`git add submodule git@github.com:AliciaGaona/hugo-theme-sam.git themes/hugo-theme-sam`


| Fragmento comando | Explicación|
| ------------ | ------- |
| __git add submodule__ | agregar nuevo submódulo|
| __git@github.com:AliciaGaona/hugo-theme-sam.git__ | url de GitHub del fork del tema(la url para clonar repositorio) |
| __themes/hugo-theme-sam__ | ruta donde se hará el submódulo |



8. Realizar commit de nuevo submódulo, el resultado sería algo así:

![image](https://user-images.githubusercontent.com/99162884/183567253-bf10bdac-cf4f-475d-aed9-af0b41f836ed.png)

9. Copiar todo el contenido que venga en ExampleSite en el repo del temay hacer commit

![image](https://user-images.githubusercontent.com/99162884/183568567-a9731270-74ad-4efc-9e10-dfd06bc6cb61.png)

__Importante__ si clonaste el repo de cero hay que inicializar y actualizar el submodulo

10. Verificar que en tu archivo de configuración se tenga el nombre del tema igual al del fihcero de submodulo creado

![2022-08-10 02_21_35-Window](https://user-images.githubusercontent.com/99162884/183839869-1e75c074-399d-4e01-b8b5-c91ac3b70c16.png)

![2022-08-10 02_22_21-Window](https://user-images.githubusercontent.com/99162884/183842185-b43cb98b-db30-4c9d-b91d-243bae673563.png)


11. Probar sitio en tu local, con el comando `hugo server`




![2022-08-10 02_24_39-Window](https://user-images.githubusercontent.com/99162884/183841852-f4974364-acbe-47ab-bc46-b3e29b19070c.png)


12. Agregar tu información, algunos temas o la mayoría te dicen donde puedes cambiarlos, subir cambios

![Captura](https://user-images.githubusercontent.com/99162884/183841967-12811aff-b3a8-4209-bc9c-d6ac60e0f781.JPG)



13. Realizar despliegue de página:
  - Crear un repositorio vacio desde GitHub(aui es donde usaremos gitPages para levantarlo)
  - Recomendación: agregarle el archivo readme.md para que no este completamente vacio y evitar errores
  - En tu repositorio HUGO(repo que tiene la información de tus post y toda la estructura del blog), aquí crearemos un submódulo en la carpeta public, este submódulo apuntará a tu repo vacío, con el siguiente comando:

 `git submodule add git@github.com:AliciaGaona/SoyAlice.git public`
 
14. Verifica que el submódulo se creo de forma correcta, se tiene que ver algo así:

![image](https://user-images.githubusercontent.com/99162884/183966332-57637606-da7e-49c6-b6b1-448edd687457.png)

15. Contruye tu sitio conm HUGO, esto se refiere a que HUGO tomará lo ue necesita de tu repositorio con todo el contenido y lo pondrá en este repo vacío, utiliza el comando  `hugo -D`

![hugooo](https://user-images.githubusercontent.com/99162884/183971327-b4da9233-e5b6-4a39-9faa-97b90ee9113f.JPG)
 aqui podemos observar como HUGO agrego todos estos archivos en public.
 
16. Entra a la carpeta public donde esta el submódulo que apunta a todo este repo con la información necesaria que HUGO necesita para levantar el sitio,y realiza un commit de los cambios.

![image](https://user-images.githubusercontent.com/99162884/183972548-fe9b731b-4caf-46bb-884b-9565c74d5f81.png)

17. Sal de public y realiza un commit para que se actualicé el id de commit de public y tengamos una unión correcta.

![commitpublic](https://user-images.githubusercontent.com/99162884/183973164-2a395e37-d969-44d2-b324-ca4a3c09dfb2.JPG)

18. Entra a tu repo donde levantaremos el sitio y activa el git Pages.
 
  
 


