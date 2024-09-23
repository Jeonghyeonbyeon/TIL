# 📅 2024-09-23 주제 : Collider

## 1. 설명
- **무엇을 배웠는가?**  
  Unity의 Collider 컴포넌트는 오브젝트 간의 충돌을 감지하는 역할을 합니다. Collider는 물리적인 상호작용 없이 충돌만을 감지할 수 있으며, BoxCollider, SphereCollider, CapsuleCollider 등 여러 가지 유형이 있습니다. Rigidbody와 함께 사용될 때, 충돌 감지가 물리적 반응으로 이어집니다.

## 2. 코드 예시
- **관련 코드 스니펫이나 예제**  
  BoxCollider를 사용하여 오브젝트 간의 충돌을 감지하는 간단한 예제입니다.

  ```csharp
  void OnCollisionEnter(Collision collision)
  {
      // 다른 오브젝트와 충돌했을 때 실행되는 코드
      if (collision.gameObject.tag == "Enemy")
      {
          Debug.Log("Enemy hit!");
      }
  }

  void OnTriggerEnter(Collider other)
  {
      // 트리거를 통해 오브젝트가 충돌했을 때 실행되는 코드
      if (other.gameObject.tag == "PowerUp")
      {
          Debug.Log("PowerUp collected!");
      }
  }
## 3. 학습한 방법
- **이 주제를 어떻게 배웠는가?**  
  Unity 공식 문서와 온라인 튜토리얼을 통해 Collider의 기본 개념을 배웠습니다.

- **유용했던 자료** : Collider 관련 Unity 문서와 여러 실습 예제가 도움이 되었습니다.  
  - [Unity Collider 공식 문서](https://docs.unity3d.com/ScriptReference/Collider.html)

## 4. 느낀 점 & 팁
- **학습하면서 느낀 점이나 주의할 점**  
  Collider를 사용할 때는 오브젝트의 크기와 모양이 충돌 감지에 큰 영향을 미칩니다. 또한 `isTrigger` 속성을 활성화하면 오브젝트가 물리적으로 상호작용하지 않고도 충돌을 감지할 수 있습니다. Rigidbody와 함께 사용하면 더욱 다양한 물리적 반응을 구현할 수 있습니다.

### 팁
- `isTrigger`를 활성화하면 충돌 대신 이벤트 트리거만 감지할 수 있습니다.
- Collider는 보통 `Rigidbody`와 함께 사용되며, 그렇지 않을 경우 물리적 반응이 없을 수 있습니다.
- 충돌하는 오브젝트의 `Layer` 설정을 통해 특정 오브젝트끼리만 충돌을 감지할 수 있습니다.

## 5. 관련 주제 링크
- [Unity Collider 컴포넌트 공식 문서](https://docs.unity3d.com/ScriptReference/Collider.html)
- [Unity 트리거 이벤트 예제](https://docs.unity3d.com/Manual/CollidersOverview.html)
