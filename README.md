# 🥇 Creacion de Proyecto 4 Capas C#
## 🎱 PASOS A SEGUIR:
### ⚓ CREACION DEL PROYECTO; API, LIBRERIAS Y REFERENCIAS
+ Primero debeos crear la solucion (sln), esta es donde almacenamos las clases y todo el proyecto.
  
  ```dotnet new sln```
  
+ Luego debemos crear el API

  ```dotnet new webapi -o {NombreAPI}```
  
+ Luego debemos agregar el API a la solucion

   ```dotnet sln add ./API```
  
+ Despues debemos crear las classlib que son librerias de clases

   ```dotnet new classlib -o Aplicacion```
  
   ```dotnet new classlib -o Dominio```
  
   ```dotnet new classlib -o Persistencia```
  
+ Agregamos las classlib a la solucion:

  ```dotnet sln add ./Aplicacion```
  
  ```dotnet sln add ./Dominio```

  ```dotnet sln add ./Persistencia```
+ Podemos ejecutar el siguiente comando para ver lo que tenemos agregado a la solucion:

  ```dotnet sln list```
+ Ahora debemos agregar las referencias:
  
  - API > Aplicacion
    
  ```cd ./API```

  ```dotnet add reference ../Aplicacion```
+ Y tambien referenciamos:
  - Aplicacion > Dominio, Persistencia 

    ```cd ..```

    ```cd ./Aplicacion```

    ```dotnet add reference ../Dominio```

    ```dotnet add reference ../Persistencia```
    
### ⚛️ INSTALACION DE PAQUETES NECESARIOS:

+ Dentro del Vscode, vamos a utilizar una extension llamada Nuget y instalamos los siguientes paquetes:
  
  - Paquetes necesarios en WebAPI:
    * AspNetCoreRateLimit
    * AutoMapper.Extensions.Microsoft.DependencyInject
    * Microsoft.AspNetCore.Authentication.JwtBearer
    * Microsoft.AspNetCore.Mvc.Versioning
    * Microsoft.AspNetCore.OpenApi
    * Microsoft.EntityFrameworkCore.Design
  - Paquetes necesarios en Dominio:
    * FluentValidation.AspNetCore
    * itext7.pdfhtml
    * Microsoft.EntityFrameworkCore
  - Paquetes necesarios en Persistencia:
    * Microsoft.EntityFrameworkCore
    * Pomelo.EntityFrameworkCore.MySql

### 🏹 CONEXION CON LA BASE DE DATOS:

+ Abrimos el appsettings.Development.json y appsettings.json
  
