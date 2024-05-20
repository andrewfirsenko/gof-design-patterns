# Design Patterns GoF

## Creational

## Structural

## Behavioral
### Strategy
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

### Observer
  > [!IMPORTANT]
  > Определяет отношение "один ко многим" между обьектами таким образом, что при изменении состояния одного обьекта происходит оповещение и обновление всех зависимых обьектов

    <details>
  <summary>Пример реализации</summary>

  Какой то пример
  
  ```swift
  Some code example
  ```
  </details>

