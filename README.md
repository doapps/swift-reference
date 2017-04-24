# Buenas prácticas de desarrollo Swift

Lorem


## Estructura del proyecto

### Estructura base sin pod
```
├─ AppName
│  ├─ AppName
│  │  └─ Helper
│  │  └─ Networking
│  │  └─ Model
│  │  └─ Extension
│  │  └─ Controller
│  │  └─ Storage
│  │  └─ View
│  │  └─ Resources
│  │  └─ InAppPurchase
│  ├─ AppNameTests
│  ├─ AppNameUITests

```

### Estructura - Helper
```
* Esta carpeta contiene bibliotecas de terceros y utilitarios.

├─ Helper
│  ├─ Libs
│  └─ Util

```
### Estructura - Networking
```
* Esta carpeta contiene todo lo relacionado a consumo de servicios web o tareas asociadas a internet.
** En el caso de existir más una modalidad de consumo se crearán las carpetas respectivas.
*** Se agruparán los servicios en relación al modelo asociado.


├─ Networking
│  ├─ Services
│  |   ├─ Rest
│  |   |   └─ ModelService.swift
│  |   └─ Soap
│  |   |   └─ OtherService.swift
│  └─ Sockets
│  |       └─ ModelSocket.swift

```

### Estructura - Model
```
* Esta carpeta contiene todo los modelos y serán nombrado en su forma básica.

├─ Model
│  └─ Event.swift

```

### Estructura - Extension
```
* Esta carpeta contiene ...

├─ Extension
│  └─ PENDIENTE

```

### Estructura - Controller
```
* Esta carpeta contiene todo los ViewController y serán agrupados en carpetas a discreción.

├─ Controller
│  └─ NameViewController.swift

```

### Estructura - Storage
```
* Esta carpeta contiene todo lo relacionado a almacenamiento local.

├─ Storage
│  └─ CoreData
│  └─ SQLite
│  └─ Preference


```

### Estructura - Resources
```
* Esta carpeta contiene todos los assest externos de la app, tales como imágenes, fonts y property list.

├─ Resources
│  └─ Assets.xcassets
│  └─ Fonts
│  └─ Files

```

### Estructura - View
```
* Esta carpeta contiene todo lo relacionado a almacenamiento local.
* Sotryboard: Considerar la grupación de UIViewController por módulos, y por cada módulo crear un .storyboard.
* Folder: hace referencia a la agrupación de vistas customizadas dentro de un ViewController
* General: contiene los componentes customizados que se reutilizan en todas la aplicación o en más de un ViewController.
* En el caso de los elementos tales como botones y labels el nombre será a discreción del desarrollador(redButton, redRegularButton, etc).


├─ View
│  └─ Storyboard
│      └─ LaunchScreen.storyboard
│      └─ Main.storyboard
│  └─ Custom
│      └─ Folder
│          └─ Cell
│          └─ Button
│          └─ Alert
│      └─ General
│          └─ Cell
│          └─ Button
│          └─ Alert


```

### Estructura - InAppPurchase
```
* Esta carpeta contiene todo lo relacionado los componentes relacionados con StoreKit framework

├─ InAppPurchase
│  └─ *


```

