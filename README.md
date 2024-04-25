# Design Patterns GoF

## Creational
* Abstract Factory
* Builder
* [Factory Method](Creational/FactoryMethod.md)
  
  > Определяет интерфейс для создания объекта, но оставляет подклассам решение о том, какой класс инстанцировать. Фабричный метод позволяет классу делегировать инстанцирование подклассам
  
* Prototype
* [Singleton](Creational/Singleton.md)

  > Гарантирует, что в приложении существует не более одного экземпляра данного класса
  
* Object Pool

## Structural

## Behavioral
* ### Strategy
  > Обеспечивает взаимозаменяемость семейства алгоритмов, даже во время выполнения.<br>
  Позволяет сделать код более гибким, тк мы не привязываемся к конкретной реализации.

  <details>
  <summary>Пример реализации</summary>

  <br>Мы хотим добавить для игрока возможность наносить удар.
  <br>Но мы не будем завязываться на конкретный удар, его конкретная реализация нас не волнует
  
  ```swift
  protocol IAttackStrategy {
    func attack()
  }

  class User {
    var attackStategy: IAttackStrategy

    func attack() {
      attackStategy.attack()
    }
    ...
  }

  class ConcreteAttack: IAttackStrategy {
    func attack() {
      ...
    }
  }
  ```
  </details>

