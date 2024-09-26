# 📅 2024-09-26 주제 : 상수 (const)

## 1. 설명
- **무엇을 배웠는가?**  
  C#에서 `const`는 변하지 않는 값을 나타내며, 한 번 정의되면 수정할 수 없는 상수를 선언하는 데 사용됩니다. 주로 프로그램의 전반에서 사용되는 불변 데이터를 저장할 때 유용합니다.

## 2. 코드 예시
- **관련 코드 스니펫이나 예제**  
  다음은 `const`를 활용한 예제입니다.
  ```csharp
  // const 예시
  const int MaxHealth = 100;
  const string Title = "100-Days-Survival";

  void Start()
  {
      Debug.Log($"게임 제목 : {Title}, 최대 체력 : {MaxHealth}");
  }
## 3. 학습한 방법
- **이 주제를 어떻게 배웠는가?**  
  게임 개발 중 전역적으로 사용되는 고정된 값을 관리하기 위해 `const`를 활용하게 되었으며, 상수를 이용한 코드 가독성 및 유지보수성을 높이는 방법에 대해 배웠습니다.

- **유용했던 자료** :  
  - [C# const 공식 문서](https://learn.microsoft.com/ko-kr/dotnet/csharp/language-reference/keywords/const)

## 4. 느낀 점 & 팁
- **학습하면서 느낀 점이나 주의할 점**  
  `const`는 변경되지 않는 값이므로 프로그램 설계 시 명확하게 정의하는 것이 중요합니다. 또 `const`는 컴파일 타임 상수이므로 런타임에 동적 변하지 않는 값에 사용해야합니다.

### 팁
- `const`는 변하지 않는 데이터에 적합합니다. 또 여러 곳에서 반복적으로 사용되는 값에는 의미를 더 명확하게 나타낼 수 있습니다.

## 5. 관련 주제 링크
- [C# const 공식 문서](https://learn.microsoft.com/ko-kr/dotnet/csharp/language-reference/keywords/const)