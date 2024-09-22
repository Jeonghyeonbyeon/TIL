# 📅 2024-09-22 주제 : Rigidbody

## 1. 설명
- **무엇을 배웠는가?**  
  Unity의 Rigidbody 컴포넌트는 물리적인 움직임을 제어하고, 중력 및 충돌을 처리하는 데 사용됩니다. 오브젝트에 Rigidbody를 추가하면, Unity의 물리 엔진이 적용되어 실시간으로 물리적 상호작용을 할 수 있습니다.

## 2. 코드 예시
- **관련 코드 스니펫이나 예제**  
  Rigidbody를 사용하여 오브젝트를 중력에 반응하게 하고, 특정 방향으로 힘을 가하는 예제입니다.

  ```csharp
  // Rigidbody 컴포넌트 선언
  Rigidbody rb;

  void Start()
  {
      // Rigidbody 컴포넌트 가져오기
      rb = GetComponent<Rigidbody>();

      // 초기 힘을 x축 방향으로 가함
      rb.AddForce(Vector3.right * 500f);
  }

  void Update()
  {
      // 점프 기능 (Space를 눌렀을 때)
      if (Input.GetKeyDown(KeyCode.Space))
      {
          rb.AddForce(Vector3.up * 300f);
      }
  }

## 3. 학습한 방법
- **이 주제를 어떻게 배웠는가?**  
  Unity의 공식 문서와 Unity Physics 관련 포럼에서 학습했습니다. Rigidbody와 물리 엔진의 연동 부분에 대해 여러 예제를 통해 실습했습니다.

  - **유용했던 자료** : Unity 공식 문서의 Rigidbody 컴포넌트 섹션은 특히 유용했습니다.  
  - [Unity Rigidbody 공식 문서](https://docs.unity3d.com/ScriptReference/Rigidbody.html)

## 4. 느낀 점 & 팁
- **학습하면서 느낀 점이나 주의할 점**  
  Rigidbody를 사용할 때 중요한 점은 오브젝트의 무게와 충돌 감지 설정입니다. `Mass`(질량)를 적절히 설정하지 않으면 오브젝트가 예상치 못한 방식으로 움직일 수 있습니다. 또한, `isKinematic` 속성을 잘못 설정하면 물리 효과가 비활성화되니, 상태를 정확하게 설정해야 합니다.

  ### 팁
  - `Use Gravity` 옵션이 활성화되어 있지 않으면 오브젝트가 중력의 영향을 받지 않습니다.
  - 충돌 처리를 보다 세밀하게 제어하려면 `Constraints` 설정을 사용하여 특정 축의 움직임을 고정할 수 있습니다.

## 5. 관련 주제 링크
- [Unity Rigidbody 컴포넌트 공식 문서](https://docs.unity3d.com/ScriptReference/Rigidbody.html)
- [Unity Physics 관련 포럼](https://forum.unity.com/forums/physics.78/)