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
│  │  └─ Storyboard
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

* Folder: hace referencia a la agrupación de vistas customizadas dentro de un Storyboard
* General: contiene los componentes customizados que se reutilizan en todas la aplicación o en más de un ViewController.
* En el caso de los elementos tales como botones y labels el nombre será a discreción del desarrollador(redButton, redRegularButton, etc).


├─ View
│  └─ Folder
│     └─ Cell
│        └─ .swift
│        └─ .xib
│  └─ General
│     └─ Cell
│     └─ Button
│     └─ Alert


```

### Estructura - Storyboard
```

* Sotryboard: Considerar la grupación de UIViewController por módulos, y por cada módulo crear un .storyboard.


├─ Storyboard
│  └─ LaunchScreen.storyboard
│  └─ Main.storyboard


```

### Estructura - InAppPurchase
```
* Esta carpeta contiene todo lo relacionado los componentes relacionados con StoreKit framework

├─ InAppPurchase
│  └─ *


```


## Estructura de un ViewController

```

import UIKit

class ViewController: UIViewController {

    
	//MARK: - Constraints outlets
    @IBOutlet weak var elementBottomConstraint: NSLayoutConstraint!
    @IBOutlet weak var elementTopConstraint: NSLayoutConstraint!
    

	//MARK: - View outlets
    @IBOutlet weak var elementTextField: CustomTextField!
    @IBOutlet weak var elementButton: CustomRegisterButton!
    @IBOutlet weak var elementView: UIView!

	//MARK: - Local constans and variables
    let thisIsAConstant = 20.0
    var thisIsAVariable = 15
    
	//MARK: - ViewController override definitions
	override func viewDidLoad() {
        super.viewDidLoad()
    }
    override func viewDidDisappear(_ animated: Bool) {
        
    }
    override func viewWillLayoutSubviews() {
       
    }
    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
    }
    
	//MARK: - Actions and other outlets remaining
    @IBAction func excuteRegister(_ sender: Any) {
        
    }
    
	//MARK: - Additional functions that may be require
    func myAwesomeFunctionImplementation(){
        
    }
    
    func allowRegister(byUser user:User, andProfile profile:Profile) -> Bool{
        
        return true
    }
}

```


## Estructura de un Modelo

```
class Car{
    
    //MARK: Properties
    var name: String
    var age: Int
    
    //MARK: Initialization
    init(name: String, age: Int) {
        self.name = name
        self.age = age
    }
    
    //MARK: Methods
    func awesomeFunction(){
        
    }
    
}

```
