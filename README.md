# Design Patterns GoF

## Creational

## Structural
1. ### Decorator
  > [!IMPORTANT]
  > Позволяет динамически добавлять новое поведение (функциональность) обьектам. Гибкая альтернатива субклассированию в расширении функциональности. Другими словами оборачивает обьекты в полезные "обертки"

  <details>
  <summary>Пример реализации</summary>

  <br>К примеру у нас есть слой CALayer с какой то реализацией. И мы можем с помощью декоработа наполнять его доп свойствами
  <br>Грубо говоря оборачиваем
  
  ```swift
  class BaseLayer: CALayer {
    func draw() {
      // Draw
    }
  }

  class Decorator: BaseLayer {
    let baseLayer: BaseLayer
  }

  class MyDecorator: Decorator {
    func draw() {
      baseLayer.draw()
      // new draw
    }
  }
  ```
  </details>

## Behavioral
1. ### Strategy
  > [!IMPORTANT]
  > Обеспечивает взаимозаменяемость семейства алгоритмов, даже во время выполнения. Позволяет сделать код более гибким, тк мы не привязываемся к конкретной реализации.

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

2. ### Observer
  > [!IMPORTANT]
  > Определяет отношение "один ко многим" между обьектами таким образом, что при изменении состояния одного обьекта происходит оповещение и обновление всех зависимых обьектов

  <details>
  <summary>Пример реализации</summary>

  Какой то пример
  
  ```swift
  Some code example
  ```
  </details>

