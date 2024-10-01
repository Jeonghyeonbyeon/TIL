# 📅 2024-10-01 주제 : 리스트 (List<T>)

## 1. 설명
- **무엇을 배웠는가?**  
  `List<T>`는 C#에서 제공하는 제네릭 컬렉션으로, 동적 크기의 배열처럼 사용할 수 있는 클래스입니다. `List<T>`는 데이터를 순차적으로 저장하고, 배열과 달리 크기를 동적으로 변경할 수 있어 편리합니다. `T`는 리스트에 저장될 데이터 타입을 나타냅니다.

## 2. 코드 예시
- **관련 코드 스니펫이나 예제**  
  다음은 `List<int>`를 사용하는 예제입니다.
  ```csharp
  using System.Collections.Generic;
  using UnityEngine;

  public class ListExample : MonoBehaviour
  {
      void Start()
      {
          List<int> numbers = new List<int>();

          // 리스트에 값 추가
          numbers.Add(1);
          numbers.Add(2);
          numbers.Add(3);

          // 리스트 값 출력
          foreach (int number in numbers)
          {
              Debug.Log(number);
          }

          // 리스트에서 값 제거
          numbers.Remove(2);

          // 다시 출력
          foreach (int number in numbers)
          {
              Debug.Log(number);
          }
      }
  }
## 3. 학습한 방법
- **이 주제를 어떻게 배웠는가?**  
  동적 데이터 저장의 필요성을 느껴서 C#에서 배열과 비슷하면서 더 유연한 자료 구조인 `List<T>`에 대해 학습했습니다. 제네릭의 개념을 익히고 다양한 타입을 리스트로 다룰 수 있는 방법을 배웠습니다.

- **유용했던 자료**:  
  - [C# List<T> 공식 문서](https://learn.microsoft.com/ko-kr/dotnet/api/system.collections.generic.list-1?view=net-7.0)

## 4. 느낀 점 & 팁
- **학습하면서 느낀 점이나 주의할 점**  
  리스트는 배열과 달리 동적으로 크기가 변하므로 관리가 쉽지만, 크기 조정에 따른 성능 오버헤드가 발생할 수 있으므로 필요한 크기만큼 `Capacity`를 설정하는 것이 성능 향상에 도움이 될 수 있습니다.

### 팁
- `List<T>`에서 빈번한 삽입이나 삭제 작업이 이루어질 경우 성능에 영향을 줄 수 있습니다. 이런 경우 `LinkedList<T>`를 고려해볼 수 있습니다.

## 5. 관련 주제 링크
- [C# List<T> 공식 문서](https://learn.microsoft.com/ko-kr/dotnet/api/system.collections.generic.list-1?view=net-7.0)