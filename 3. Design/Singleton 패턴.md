# 📅 2024-09-24 주제 : Singleton 패턴

## 1. 설명
- **무엇을 배웠는가?**  
  Singleton 패턴은 클래스의 인스턴스가 하나만 생성되도록 보장하고, 전역적으로 그 인스턴스에 접근할 수 있는 디자인 패턴입니다. 주로 게임 개발에서 게임 관리 객체(Game Manager), 오디오 관리 객체(Audio Manager) 등 전역적인 데이터를 관리하는 데 사용됩니다.

## 2. 코드 예시
- **관련 코드 스니펫이나 예제**  
  다음은 C#에서 Singleton 패턴을 구현한 예제입니다.

  ```csharp
  public class GameManager : MonoBehaviour
  {
      // Singleton 인스턴스
      private static GameManager instance;

      // 인스턴스로 접근하기 위한 프로퍼티
      public static GameManager Instance
      {
          get
          {
              if (instance == null)
              {
                  // GameManager 없을 경우 새로 생성
                  instance = FindObjectOfType<GameManager>();

                  if (instance == null)
                  {
                      GameObject singleton = new GameObject("GameManager");
                      instance = singleton.AddComponent<GameManager>();
                  }
              }
              return instance;
          }
      }

      private void Awake()
      {
          // 인스턴스가 이미 존재하면 삭제
          if (instance != null && instance != this)
          {
              Destroy(gameObject);
              return;
          }

          // 인스턴스를 유지
          instance = this;
          DontDestroyOnLoad(gameObject); // 씬 전환 시에도 싱글톤 오브젝트 유지
      }
  }
## 3. 학습한 방법
- **이 주제를 어떻게 배웠는가?**  
  Singleton 패턴은 Unity 게임 개발에서 자주 사용되기 때문에 YouTube 싱글톤 패턴 강좌를 보며 공부했습니다.

- **유용했던 자료** :  
  - [베르의 게임 개발 유튜브 : 싱글톤 패턴 구현하기](youtube.com/watch?v=-wzULWMvFu0)

## 4. 느낀 점 & 팁
- **학습하면서 느낀 점이나 주의할 점**  
  Singleton 패턴은 유용하지만 남용할 경우 코드의 복잡하게 만들수 있습니다. 또 멀티스레딩 환경에서 사용 시 주의해야 하고, 게임에서의 리소스 관리 객체나 게임 상태 관리에 적합합니다.

### 팁
- `DontDestroyOnLoad` 메서드를 사용하면 씬이 전환될 때도 Singleton 객체를 유지할 수 있습니다.
- 필요하지 않은 경우, Singleton을 남용하지 않도록 주의해야 합니다.

## 5. 관련 주제 링크
- [베르의 게임 개발 유튜브 : 싱글톤 패턴 구현하기](youtube.com/watch?v=-wzULWMvFu0)