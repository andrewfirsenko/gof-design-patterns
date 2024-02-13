### Factory Method

**Описание:** <br>
Это шаблон который предоставляет интерфейс для создания объектов. Фабричный метод инкапсулирует создание обьектов в одном месте

**Когда:** <br>
Фабричный метод полезен, когда у нас есть обьекты, которые имеют общее поведение или свойсва, но имеют разные реализации.
Так же когда для создания обьекта необходими зависимости. Мы можем их инкапсулировать в фабрику

**Как выглядит:**

**Пример:**

```swift
// Протокол конфеты
protocol ICandy {
	func eat()
}

// Конкретные конфеты
struct CandyA: ICandy {
	func eat() { print("CandyA... ate") }
}

struct CandyB: ICandy {
	func eat() { print("CandyB... ate") }
}

// Протокол фабрики
enum CandyType {
	case candyA
	case candyB
}

protocol ICandyFactory {
	func makeCandy(type: CandyType) -> ICandy
}

// Конкретная фабрика
class CurrentFactory: ICandyFactory {
	func makeCandy(type: CandyType) -> ICandy {
		switch type {
			case .candyA: return CandyA()
			case .candyB: return CandyB()
		}
	}
}

// Применение
let factory = CurrentFactory()

let candyA = factory.makeCandy(type: .candyA)
let candyB = factory.makeCandy(type: .candyB)

candyA.eat()
candyB.eat()
```

