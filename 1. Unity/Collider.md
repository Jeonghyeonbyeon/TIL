# 📅 2024-09-23 주제 : Collider

## 1. 설명
- **무엇을 배웠는가?**  
  Unity에서 Collider는 오브젝트의 물리적인 상호작용, 충돌을 관리한다. 대표적인 Collider로는 BoxCollider, SphereCollider, CapsuleCollider 등이 있다. 여기서 물리적인 상호작용은 Rigidbody 컴포넌트를 추가해야 사용이 가능하다.

## 2. 코드 예시
- **관련 코드 스니펫이나 예제**  
  BoxCollier를 사용하여 간단하게 충돌을 체크하는 코드 예제입니다.

  ```csharp
  void OnCollisionEnter(Collision collision)
  {
      // Enemy 태그를 가진 오브젝트와 충돌했을 때 실행되는 코드
      if (collision.gameObject.tag == "Enemy")
      {
          Debug.Log("Enemy 충돌!");
      }
  }

  void OnTriggerEnter(Collider other)
  {
      // PowerUp 태그를 가진 트리거 오브젝트와 충돌했을 때 실행되는 코드
      if (other.gameObject.tag == "PowerUp")
      {
          Debug.Log("PowerUp 성공!");
      }
  }
## 3. 학습한 방법
- **이 주제를 어떻게 배웠는가?**  
  YouTube 강의와 Unity에서 직접 사용해보면서 공부했습니다.

- **유용했던 자료** : Collider 관련 유튜브 강의 영상이 도움이 되었다.  
- [베르의 게임 개발 유튜브 : 콜라이더의 기본](https://www.youtube.com/watch?v=wW6vgmxTDvY)

## 4. 느낀 점 & 팁
- **학습하면서 느낀 점이나 주의할 점**  
  `isTrigger` 속성을 활성화하면 오브젝트가 물리적으로 상호작용하지 않고 충돌을 감지할 수 있습니다. Rigidbody 컴포넌트와 함께 사용한다면 더욱 더 다양한 물리 구현이 가능하다.

### 팁
- `isTrigger`를 활성화하면 충돌 대신 이벤트 트리거만 감지할 수 있다.
- Collider는 보통 `Rigidbody`와 함께 사용되고, 만약 Rigidbody가 없다면 물리적 반응이 없을 수 있다.
- `Layer` 설정을 통해 특정 오브젝트끼리만 충돌을 감지할 수 있다.

## 5. 관련 주제 링크
- [Unity Collider 컴포넌트 공식 문서](https://docs.unity3d.com/ScriptReference/Collider.html)
- [베르의 게임 개발 유튜브 : 콜라이더의 기본](https://www.youtube.com/watch?v=wW6vgmxTDvY)
