## <Java 기초>
### 인스턴스와 클래스
- 오브젝트 도출 순서
   * 각 오브젝트의 속성, 동작에 대한 종류와 내용 정의
   * 가상세계에 도출, 동작시키기
- 용어정리
   - 오브젝트 (object) : 현실 세계의 모든 객체
   - 클래스 (class) : 오브젝트를 가상세계 용으로 구체화 (틀, 설계도)
   - 인스턴스 (instance) : 클래스를 활용해 메모리 상에 만든 것 (실체)

***

### 필드와 메소드
|   클래스 명   |   명사   |      단어의 맨 처음은 대문자 (pascal)      |              Hero, MonsterInfo               |
|:---------:|:------:|:--------------------------------:|:--------------------------------------------:|
| **필드 명**  | **명사** | **최초 이외의 단어의 맨 처음은 대문자 (camel)** | **mLevel, mItemList,level, items, itemList** |
| **메소드 명** | **동사** | **최초 이외의 단어의 맨 처음은 대문자 (camel)** |          **attack, findWeakPoint**           |
 
- #### 클래스를 코드로 표현
    ```java
    public class Hero {  //용사
        String name;                 //이름
        int hp;                      //HP
  
        void attack()  {}            //싸우기
        void run()  {}               //도망 
        void sit(int sec)  {}        //앉기
        void slip()  {}              //넘어지기 
        void sleep()  {}             //잠자기
    }
  ```

- #### 필드를 상수로 선언
    ```java
    public class Kinoko {
        int hp;
        final int level = 10;
    }
    ```
  
- #### 'this'는 자기 자신을 가리킴
    자기 자신에게 접근할 수 있는 주소
    ```java
    void sleep() {
        this.hp = 100;
        System.out.println(this.name + "는 잠을 자고 회복했다!");
    }
    ```
  
 ***

### 클래스 타입
- 클래스를 정의 -> 클래스 타입의 변수를 선언할 수 있음
- 그 클래스의 인스턴스를 담을 수 있음

> #### 클래스 왜 만들어?
> - 각 객체의 고유 속성, 기능이 있으니까
> - 현실세계에 대입해서 그대로 표현한다면 class를 쓰는 게 개발자가 이해하기 쉬움
> - 메모리, 속도 등 성능 측면에서 장점이 없지만, 이해하기 쉽고 버그 발생률 줄어듦
> - 속도보다 안정성, 유지보수가 더 중요

***

### 인스턴스화
+ new를 사용해서 인스턴스 생성
  + new : 원래 사용될지 모르는데 실행되면서 메모리가 할당되는것(크기랑 상관 없음)
+ **“변수명.필드명”, “변수명.메소드명()”** 으로 인스턴스의 필드나 메소드 이용
    ```java
    Hero hero = new Hero();
    hero.name = "민지";
    hero.hp = 100;
    ```
