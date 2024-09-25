# 📅 2024-09-22 주제 : Rigidbody

## 1. 설명
- **무엇을 배웠는가?**  
  Unity의 Rigidbody 컴포넌트를 적용하면 물리적 제어를 받습니다. 또 중력과 충돌 제어에 사용됩니다.

## 2. 코드 예시
- **관련 코드 스니펫이나 예제**  
  Rigidbody 컴포넌트를 사용해서 오브젝트에 중력을 적용 후 x축으로 힘을 가하고 Space 키를 눌렀을때, 오브젝트가 위로 점프하는 예제입니다.

  ```csharp
  // Rigidbody 컴포넌트 선언
  Rigidbody rb;

  void Start()
  {
      // Rigidbody 컴포넌트 가져오기
      rb = GetComponent<Rigidbody>();

      // x축 방향으로 500만큼의 힘을 가함
      rb.AddForce(Vector3.right * 500f);
  }

  void Update()
  {
      // 점프 기능 (Space를 눌렀을 때)
      if (Input.GetKeyDown(KeyCode.Space))
      {
          // 오브젝트를 y축 방향으로 300만큼의 힘을 가함
          rb.AddForce(Vector3.up * 300f);
      }
  }
## 3. 학습한 방법
- **이 주제를 어떻게 배웠는가?**  
  Unity의 공식 문서와 YouTube 강의 영상을 통해서 공부했습니다.

- **유용했던 자료** : 케이디의 입문 강좌 Rigidbody을 보면서 직접 보면서 직접 만들어보니까 훨씬 이해에 도움이 되었다.
- [케이디 : 유니티 Rigidbody 입문 강좌](https://www.youtube.com/watch?v=V1ZcL55h3h4)

## 4. 느낀 점 & 팁
- **학습하면서 느낀 점이나 주의할 점**  
  Rigidbody를 사용할 때 중요한 점은 오브젝트의 무게와 충돌 감지 설정으로, `Mass`를 적절히 설정하지 않으면 오브젝트가 예상치 못하게 움직일 수 있습니다. 또 `isKinematic`속성 설정을 잘못 설정하면 물리효과가 비활성화 될 수 있으므로 정확하게 설정해야한다.

### 팁
- `Use Gravity` 옵션이 활성화 되어있으면 중력의 영향을 안 받습니다.
- `Constraints` 설정을 사용하여 특정 축의 움직임을 고정할 수 있습니다.

## 5. 관련 주제 링크
- [Unity Rigidbody 컴포넌트 공식 문서](https://docs.unity3d.com/ScriptReference/Rigidbody.html)
- [케이디 : 유니티 Rigidbody 입문 강좌](https://www.youtube.com/watch?v=V1ZcL55h3h4)