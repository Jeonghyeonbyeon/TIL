# 📅 2024-09-27 주제 : 클래스 (Class)

## 1. 설명
- **무엇을 배웠는가?**  
  C#에서 클래스는 객체 지향 프로그래밍의 기본 개념 중 하나로, 데이터(필드)와 기능(메서드)를 묶어 관리하는 틀입니다. 클래스를 사용하면 객체를 생성할 수 있으며, 프로그램에서 여러 개의 객체를 효율적으로 다룰 수 있습니다. 게임 개발에서 캐릭터나 아이템 등을 객체로 만들 때 유용하게 활용할 수 있습니다.

## 2. 코드 예시
- **관련 코드 스니펫이나 예제**  
  `Player` 클래스를 사용한 간단한 예제입니다.
  ```csharp
  // Player 클래스 예시
  public class Player
  {
      public string Name;
      public int Health;
      
      // 생성자
      public Player(string name, int health)
      {
          Name = name;
          Health = health;
      }
      
      // 메서드
      public void TakeDamage(int damage)
      {
          Health -= damage;
          Debug.Log($"{Name}가 {damage}만큼의 데미지를 입었습니다. 남은 체력 : {Health}");
      }
  }

  void Start()
  {
      Player player = new Player("Junghyun", 100);
      player.TakeDamage(10);
  }
## 3. 학습한 방법
- **이 주제를 어떻게 배웠는가?**  
  Unity에서 게임 캐릭터나 아이템을 다룰 때 클래스를 사용하면서 학습하게 되었습니다. 캐릭터의 속성이나 행동을 관리하기 위해 클래스를 정의하고, 그 안에서 상태를 관리하고 메서드를 통해 행동을 구현하면서 자연스럽게 익히게 되었습니다.

- **유용했던 자료** :  
  - [C# 클래스 공식 문서](https://learn.microsoft.com/ko-kr/dotnet/csharp/programming-guide/classes-and-structs/classes)

## 4. 느낀 점 & 팁
- **학습하면서 느낀 점이나 주의할 점**  
  클래스를 처음 사용할 때는 조금 복잡해 보일 수 있지만, 잘 설계된 클래스는 코드의 유지보수성을 크게 높여주고 필드와 메서드를 적절하게 설계하고 관리하면 프로그램 구조가 훨씬 깔끔해질 수 있습니다. 또 필드를 직접 접근하는 것보다 메서드를 통해 처리하는 것이 안정적이라는 점도 유의해야 합니다.

### 팁
- 생성자를 통해 객체를 초기화할 때 필요한 값을 설정하는 것이 중요합니다. 이를 통해 객체가 일관된 상태를 유지할 수 있습니다.

## 5. 관련 주제 링크
- [C# 클래스 공식 문서](https://learn.microsoft.com/ko-kr/dotnet/csharp/programming-guide/classes-and-structs/classes)