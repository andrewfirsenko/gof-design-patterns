### Singleton

**Описание:** <br>
Singleton гарантирует, что в приложении существует не более одного экземпляра данного класса.
Предоставляет глобальную точку доступа к этому обьекту

**Когда:** <br>
Singleton полезен, когда нам необходимо чтобы был один экземпляр класса. Часто когда это связано с физичискими обьектами (принтеры) или настройками и тд

**Как выглядит:**

<img src="../Images/Singleton.webp" width="80%">

**Пример:**

```swift
final class Singleton {
    
    static let shared: Singleton = Singleton()
    
    private init() {}
}

Singleton.shared // Ok

Singleton() // Not available, becase private init()
```

