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


### Estructura - View
```
* Esta carpeta contiene todo lo relacionado a almacenamiento local.

├─ View
│  └─ Storyboard
│  └─ Cell
│  └─ Assets


```

### Estructura - InAppPurchase
```
* Esta carpeta contiene todo lo relacionado los componentes relacionados con StoreKit framework

├─ InAppPurchase
│  └─ *


```

