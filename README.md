# Buenas prácticas de desarrollo Swift

La estructura que se desarrolla a continuación permitirá una correcta organización y reutilización de los componentes de software embebidos en un proyecto generado por Xcode


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
* Esta carpeta contiene bibliotecas y utilitarios que pueden ser de terceros o propios del desarrollador. Los nombres de los utilitarios desarrollados deben de ser lo suficientemente explicitos en el nombre y exponer un comentario sobre su existencia.


├─ Helper
│  ├─ Libs
│  └─ Util

```
### Estructura - Networking
```
* Esta carpeta contiene todo lo relacionado a consumo de servicios web o tareas asociadas a internet.
** En el caso de existir más una modalidad de consumo se crearán las carpetas respectivas.
*** Se creará una clase principal llamada EndPoints la cual contendra las urls usadas en el proyecto y luego se crearán extensiones de la clase mencionada que contengan la implementación de un método


├─ Networking
│  ├─ Services
│  |   ├─ Rest
│  |   |   └─ EndPoints.swift
│  |   |   └─ MethodName.swift
│  |   └─ Soap
│  |   |   └─ EndPoints.swift
│  └─ Sockets
│  |       └─ ModelSocket.swift

```

### Estructura - Model
```
* Esta carpeta contiene todo los modelos y serán nombrado en su forma básica.

├─ Model
│  └─ Protocol
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
* Esta carpeta contiene todo los ViewController y serán agrupados en subcarpetas a discreción.

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
** (Assets) Se crearán subcarpetas las cuales harán referencia a los storyboards existentes. Si un recurso es utilizado en mas de un storyboard deberá encontrarse en la carpeta llamada "General"

├─ Resources
│  └─ Assets.xcassets
│  └─ Fonts
│  └─ Files

```

### Estructura - View
```


* Dentro de la carpeta View se crearan subcarpetas que haran referencia a los distintos componentes gráficos. Dentro de estas subcarpetas se crearán los archivos .swift y .xib según sea necesario.


├─ View
│  └─ Cell
│  └─ Button
│  └─ Alert


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
