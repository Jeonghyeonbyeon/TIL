# 📅 2024-09-24 주제 : 조건문 (if, else, switch)

## 1. 설명
- **무엇을 배웠는가?**  
  C#의 조건문은 프로그램이 특정 조건을 만족할 때 코드 블록을 실행할 수 있게 합니다. 조건문은 프로그램 흐름을 제어하고, 다양한 경우에 맞춰 동작을 달리할 수 있게 해줍니다. 기본적인 조건문은 `if`, `else if`, `else`, 그리고 다중 조건 처리에는 `switch` 문이 사용됩니다.

## 2. 코드 예시
- **관련 코드 스니펫이나 예제**  
  다음은 `if-else` 문과 `switch` 문을 활용한 간단한 조건문 예제입니다.

  ```csharp
  // if-else 조건문 예시
  int playerHealth = 50;

  void CheckHealth()
  {
      if (playerHealth > 75)
      {
          Debug.Log("Player is healthy.");
      }
      else if (playerHealth > 25)
      {
          Debug.Log("Player is wounded.");
      }
      else
      {
          Debug.Log("Player is in critical condition.");
      }
  }

  // switch 문 예시
  string difficulty = "Normal";

  void SetGameDifficulty()
  {
      switch (difficulty)
      {
          case "Easy":
              Debug.Log("Game set to Easy mode.");
              break;
          case "Normal":
              Debug.Log("Game set to Normal mode.");
              break;
          case "Hard":
              Debug.Log("Game set to Hard mode.");
              break;
          default:
              Debug.Log("Unknown difficulty setting.");
              break;
      }
  }
## 3. 학습한 방법
- **이 주제를 어떻게 배웠는가?**  
  C# 공식 문서와 Unity 학습 자료를 통해 조건문을 학습했습니다. 또한, 게임 개발 중에 자주 사용되는 로직 흐름 제어를 구현하면서 조건문의 다양한 활용 방법을 실습했습니다.

- **유용했던 자료** :  
  - [C# if-else 문 공식 문서](https://learn.microsoft.com/ko-kr/dotnet/csharp/language-reference/statements/selection-statements)
  - [C# switch 문 공식 문서](https://learn.microsoft.com/ko-kr/dotnet/csharp/language-reference/statements/selection-statements#the-switch-statement)

## 4. 느낀 점 & 팁
- **학습하면서 느낀 점이나 주의할 점**  
  조건문을 사용할 때는 가능한 한 간결하게 작성하는 것이 중요합니다. 특히, 여러 개의 `else if`가 중첩될 경우 코드가 복잡해질 수 있으므로, 가능한 `switch` 문을 사용하는 것이 더 가독성이 좋습니다.

### 팁
- `switch` 문은 값이 여러 개로 나눠질 때 유용하게 사용할 수 있습니다. `if` 문보다 더 구조적으로 표현할 수 있습니다.
- 조건문에서 조건이 너무 복잡해질 경우, 로직을 메서드로 분리해 가독성을 높이는 것이 좋습니다.

## 5. 관련 주제 링크
- [C# 조건문 공식 문서](https://learn.microsoft.com/ko-kr/dotnet/csharp/language-reference/statements/selection-statements)
- [Unity C# 스크립팅 튜토리얼](https://learn.unity.com/course/create-with-code)