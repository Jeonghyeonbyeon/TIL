# 📅 2024-09-30 주제 : 소멸자 (Destructor)

## 1. 설명
- **무엇을 배웠는가?**  
  C#에서 소멸자는 객체가 가비지 컬렉션에 의해 메모리에서 제거되기 직전에 호출되는 특별한 메서드입니다. 소멸자는 클래스 이름 앞에 틸드(~) 기호를 붙여 정의하며, 인스턴스가 메모리에서 해제될 때 리소스를 해제하는 데 사용됩니다.

## 2. 코드 예시
- **관련 코드 스니펫이나 예제**  
  다음은 소멸자를 사용하는 예제입니다.
  ```csharp
  class Player
  {
      public Player()
      {
          Debug.Log("Player 객체 생성");
      }

      ~Player()
      {
          Debug.Log("Player 객체 소멸");
      }
  }

  void Start()
  {
      Player player = new Player();
  }
## 3. 학습한 방법
- **이 주제를 어떻게 배웠는가?**  
  자원 관리의 중요성을 이해하기 위해 가비지 컬렉션과 소멸자에 대해 학습했습니다. 특히 파일이나 네트워크 연결 등 중요한 리소스를 해제할 때 소멸자의 역할을 확인했습니다.

- **유용했던 자료**:  
  - [C# 소멸자 공식 문서](https://learn.microsoft.com/ko-kr/dotnet/csharp/programming-guide/classes-and-structs/destructors)

## 4. 느낀 점 & 팁
- **학습하면서 느낀 점이나 주의할 점**  
  소멸자는 명시적으로 호출할 수 없고, 가비지 컬렉터에 의해 자동으로 호출됩니다. 다만, 소멸자의 동작을 예측하기 어려우므로 리소스 해제는 가능하면 `IDisposable` 인터페이스와 `Dispose()` 메서드를 활용해 관리하는 것이 더 좋을 수 있습니다.

### 팁
- `IDisposable`과 `Dispose` 패턴을 사용하는 것이 더 명확한 자원 관리를 할 수 있는 방법입니다.

## 5. 관련 주제 링크
- [C# 소멸자 공식 문서](https://learn.microsoft.com/ko-kr/dotnet/csharp/programming-guide/classes-and-structs/destructors)