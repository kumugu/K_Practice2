

# Access Modifiers

------

## 1. 접근 제어란?

접근 제어(Access Control)는 **클래스, 변수, 메서드의 접근 범위를 설정하여 외부 접근을 제어**하는 역할을 합니다. 이는 캡슐화(encapsulation)와 정보 은닉을 실현하여 코드의 안정성을 높입니다.

## 2. 접근 제어자의 종류

1. **public**

   - 모든 클래스에서 접근이 가능합니다.

   - 코드 전체에서 공용으로 사용되는 클래스, 메서드에 사용됩니다.

     ```
     java코드 복사public class PublicClass { 
         public void publicMethod() {
             // Code
         }
     }
     ```

2. **protected**

   - 같은 패키지 내에 있거나 자식 클래스에서만 접근이 가능합니다.

   - 상속 관계에서만 접근을 허용하는 경우에 사용합니다.

     ```
     java코드 복사protected class ParentClass { 
         protected void protectedMethod() {
             // Code
         }
     }
     ```

3. **default** (패키지 접근)

   - 동일한 패키지 내에서만 접근이 가능하며, 접근 제어자를 명시하지 않으면 적용됩니다.

     ```
     java코드 복사class DefaultClass {
         void defaultMethod() {
             // Code
         }
     }
     ```

4. **private**

   - 해당 클래스 내에서만 접근이 가능합니다.

   - 캡슐화를 실현하여 외부 접근을 차단하는 목적으로 사용합니다.

     ```
     java코드 복사class PrivateClass {
         private void privateMethod() {
             // Code
         }
     }
     ```

## 3. 접근 제어의 역할

캡슐화를 통해 코드의 무결성을 보장하고, 필요한 경우에만 외부와 상호작용할 수 있게 하여 **안정성, 재사용성, 유지보수성**을 높입니다.

------



# ArrayList



## 1. ArrayList란?

`ArrayList`는 자바에서 제공하는 **동적 배열 구현 클래스**로, 크기를 유연하게 변경할 수 있는 배열입니다. `java.util.ArrayList` 패키지에서 제공되며, 크기 조정이 필요한 경우 유용하게 사용할 수 있습니다.

## 2. ArrayList 생성과 초기화

- ```
  ArrayList
  ```

  는 기본적으로 

  ```
  List
  ```

   인터페이스를 구현하며, 생성 시 초기 크기를 지정할 수 있습니다.

  ```
  java코드 복사List<String> list = new ArrayList<>(); // 기본 생성자
  List<Integer> numbers = new ArrayList<>(10); // 초기 크기 지정
  ```

## 3. 주요 메서드

1. **add()**

   - 요소를 추가합니다.

     ```
     java코드 복사list.add("Hello");
     list.add("World");
     ```

2. **get()**

   - 지정된 인덱스의 요소를 반환합니다.

     ```
     java
     
     
     코드 복사
     String element = list.get(0); // "Hello"
     ```

3. **size()**

   - 요소의 개수를 반환합니다.

     ```
     java
     
     
     코드 복사
     int count = list.size(); // 2
     ```

4. **remove()**

   - 지정된 인덱스의 요소를 제거합니다.

     ```
     java
     
     
     코드 복사
     list.remove(1); // "World" 제거
     ```

## 4. ArrayList 사용 시 주의사항

`ArrayList`는 **비동기적**이며, 다중 스레드 환경에서는 `Vector`나 `Collections.synchronizedList()`를 사용할 수 있습니다.

------



# Enhanced for Loop



## 1. 향상된 for문이란?

향상된 for문(Enhanced for loop)은 배열 또는 컬렉션 객체의 요소를 순회하는 간편한 방법입니다. 반복 변수를 통해 **요소를 하나씩 처리할 때 유용**합니다.

## 2. 향상된 for문 형식

기본 구문은 아래와 같습니다:

```
java코드 복사for (type variable : collection) {
    // Code
}
```

### 예제

배열과 `ArrayList` 순회 예제입니다.

```
java코드 복사// 배열 순회
int[] numbers = {1, 2, 3, 4, 5};
for (int num : numbers) {
    System.out.println(num);
}

// ArrayList 순회
List<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
for (String language : list) {
    System.out.println(language);
}
```

## 3. 향상된 for문의 특징

1. **간결함**
   - `for` 문에 비해 구문이 간결하여 가독성이 높습니다.
2. **읽기 전용**
   - 요소의 값을 변경할 수 없으며, 컬렉션 요소의 추가, 삭제 등의 작업은 불가능합니다.
3. **Iterator 기반**
   - 내부적으로 `Iterator`를 사용하여 순회하므로, `Iterator`와 동일한 결과를 얻을 수 있습니다.

향상된 for문은 코드의 가독성을 높이고, 오류 발생 가능성을 줄여주는 효과적인 반복문입니다.
