---
title: Q#의 형식
description: 'Q # 프로그래밍 언어에 사용 되는 다양 한 형식에 대해 알아봅니다.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
ms.openlocfilehash: e37ce6e3a2dfad5395cdecf06178d64ec51b79f1
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415289"
---
# <a name="types-in-q"></a>Q#의 형식

이 문서에서는 Q # 형식 모델 및 형식을 지정 하 고 사용 하는 구문에 대해 설명 합니다. 이러한 형식의 식을 만들고 작동 하는 방법에 대 한 자세한 내용은 [형식 식](xref:microsoft.quantum.guide.expressions)을 참조 하세요.

Q #은 *강력한* 형식의 언어 이므로 이러한 형식을 신중히 사용 하면 컴파일러가 컴파일 시간에 Q # 프로그램에 대 한 강력한 보증을 제공 하는 데 도움이 될 수 있습니다.
가장 강력한 보증을 제공 하기 위해 해당 변환을 표현 하는 함수에 대 한 호출을 사용 하 여 Q #의 형식 간 변환이 명시적 이어야 합니다. Q #에서는 네임 스페이스의 일부분으로 다양 한 함수를 제공 <xref:microsoft.quantum.convert> 합니다.
반면에 호환 되는 형식에 대 한 upcasts은 암시적으로 수행 됩니다. 

Q #에서는 직접 사용 되는 기본 형식과 다른 형식에서 새 형식을 생성 하는 다양 한 방법을 제공 합니다.
이 문서의 나머지 부분에서 각각에 대해 설명 합니다.

## <a name="primitive-types"></a>기본 유형

Q # 언어는 Q # 프로그램에서 직접 사용할 수 있는 다음과 같은 *기본 형식을*제공 합니다. 이러한 기본 형식을 사용 하 여 새 형식을 생성할 수도 있습니다.

- `Int`형식은 64 비트 부호 있는 정수를 나타냅니다 (예:,, `2` ) `107` `-5` .
- `BigInt`형식은 임의 크기의 부호 있는 정수를 나타냅니다 (예:,,) `2L` `107L` `-5L` .
   이 형식은 .NET을 기반으로 합니다.<xref:System.Numerics.BigInteger>
   입력할.

- `Double`형식은 배정밀도 부동 소수점 숫자를 나타냅니다 (예:,,) `0.0` `-1.3` `4e-7` .
- `Bool`형식은 또는의 부울 값을 나타냅니다 `true` `false` .
- `Range`형식은에 의해 표시 되는 정수 시퀀스를 나타냅니다 `start..step..stop` . 여기서 단계는 선택 사항입니다. 
   예를 들어는 `start .. stop` 에 해당 하 `start..1..stop` 고 `1..2..7` 는 $ \{ 1, 3, 5, 7 $ 시퀀스를 나타냅니다 \} .
- `String`형식은 사용자가 만든 후 불투명 한 유니코드 문자 시퀀스입니다.
  `string`오류 또는 진단 이벤트의 경우 유형을 사용 하 여 메시지를 클래식 호스트에 보고 합니다.
- 형식에는 `Unit` 하나의 값만 사용할 수 있습니다 `()` . 
  이 형식을 사용 하 여 Q # 함수 또는 연산이 정보를 반환 하지 않음을 나타낼 수 있습니다. 
- `Qubit`형식은 퀀텀 비트 또는 비트를 나타냅니다.
   `Qubit`는 사용자에 게 불투명 합니다. 다른 작업에 전달 하는 것 외에도 가능한 유일한 작업은 id (같음)를 테스트 하는 것입니다.
   궁극적으로 `Qubit` 는 퀀텀 프로세서 (또는 퀀텀 시뮬레이터)에서 내장 명령을 호출 하 여에 대 한 작업을 구현 합니다.
- `Pauli`형식은 4 개의 단일 기능 비트 Pauli 연산자 중 하나를 나타냅니다.
   이 형식을 사용 하 여 회전의 기본 연산을 나타내고 측정 가능한 관찰 가능를 지정 합니다.
   `PauliI` `PauliX` 형식 상수인,, `PauliY` 및 `PauliZ` 의 네 가지 가능한 값을 가진 열거형 형식입니다 `Pauli` .
- `Result`형식은 측정 결과를 나타냅니다.
   이는 두 가지 가능한 값인 및 (형식의 상수인)를 사용 하는 열거형 형식입니다 `One` `Zero` `Result` .
   `Zero`+ 1 eigenvalue를 측정 했음을 나타냅니다. `One`-1 eigenvalue를 측정 했음을 나타냅니다.

상수 `true` ,,,,,, `false` 및는 `PauliI` `PauliX` `PauliY` `PauliZ` `One` `Zero` Q #의 모든 예약 된 기호입니다.

## <a name="array-types"></a>배열 유형

* 유효한 Q # 형식의 경우 해당 형식의 값 배열을 나타내는 형식이 있습니다.
    예를 들어 `Qubit[]` 및는 `(Bool, Pauli)[]` `Qubit` 값과 튜플 값의 배열을 나타냅니다 `(Bool, Pauli)` .

* 배열의 배열도 유효 합니다. 앞의 예제에서 확장 하면 배열의 배열이 표시 `(Bool, Pauli)` 됩니다 `(Bool, Pauli)[][]` .

> [!NOTE] 
> 이 예제는 `(Bool, Pauli)[][]` 사각형 2 차원 배열이 아니라 잠재적으로 가변 배열 배열을 나타냅니다. Q #에서는 사각형 다차원 배열을 지원 하지 않습니다.

* 에서와 같이 배열의 요소 주위에 대괄호를 사용 하 여 Q # 소스 코드에서 배열 값을 작성할 수 있습니다 `[PauliI, PauliX, PauliY, PauliZ]` .
배열의 모든 항목에 대 한 공통 기본 형식은 배열 리터럴의 형식을 결정 합니다. 따라서 공통 된 기본 형식이 없는 요소를 사용 하 여 배열을 생성 하면 오류가 발생 합니다.  
예제는 [callables 배열](xref:microsoft.quantum.guide.expressions#arrays-of-callables)을 참조 하세요.

    > [!WARNING]
    > 배열의 요소를 만든 후에는 변경할 수 없습니다.
    > 수정 된 배열을 생성 하려면 [업데이트 및 재할당 문이나](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) [복사 및 업데이트 식을](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions)사용 합니다.

* 또는 키워드를 사용 하 여 크기에서 배열을 만들 수 있습니다 `new` .

    ```qsharp
    let zeros = new Int[13];
    // you can also use new for creating empty arrays:
    let emptyRegister = new Qubit[0];
    ```

* 핵심 함수를 사용 `Length` 하 여 배열의 요소 수를로 가져옵니다 `Int` .
* 배열을 첨자 하 여 배열 요소의 하위 집합을 포함 하는 단일 요소나 새 배열을 가져올 수 있습니다.
배열의 첨자는 0부터 시작 하며 형식 또는 형식 이어야 합니다 `Int` `Range` .

    ```qsharp
    let arr = [10, 11, 36, 49];
    let ten = arr[0]; // 10
    let odds = arr[1..2..4]; // [11, 49]
    ```

## <a name="tuple-types"></a>튜플 형식

튜플은 값을 단일 값으로 수집 하 여 보다 쉽게 전달할 수 있도록 Q # 전체에서 사용 되는 강력한 개념입니다.
특히 튜플 표기법을 사용 하면 모든 작업 및 호출 가능에서 정확히 하나의 입력을 사용 하 고 정확히 하나의 출력을 반환 하도록 표현할 수 있습니다.

* 0 개 이상의 다른 형식 `T0` ,, ...,이 지정 된 경우 `T1` `Tn` 새 *튜플 형식을* 로 나타낼 수 `(T0, T1, ..., Tn)` 있습니다.
에서와 같이 새 튜플 형식을 생성 하는 데 사용 되는 형식은 튜플이 될 수 있습니다 `(Int, (Qubit, Qubit))` .
그러나 이러한 중첩은 항상 유한 하지만 튜플 형식은 어떤 경우에도 자체적으로 포함 될 수 없습니다.

* 새 튜플 형식의 값은 튜플의 각 형식에서 값의 시퀀스로 구성 된 튜플입니다.
예를 들어 `(3, false)` 는 튜플 유형인 형식의 튜플입니다 `(Int, Bool)` .
튜플, 배열의 튜플, 하위 튜플 튜플 등의 배열을 만들 수 있습니다.

* Q # 0.3를 사용 하 여 `Unit` 은 빈 튜플의 *형식* 이름입니다 .는 `()` 빈 튜플의 *값* 에 사용 됩니다.

* 튜플 인스턴스는 변경할 수 없습니다.
Q #에서는 생성 된 튜플의 콘텐츠를 변경 하는 메커니즘을 제공 하지 않습니다.



### <a name="singleton-tuple-equivalence"></a>단일 튜플 동등성

또는와 같은 singleton (단일 요소) 튜플을 만들 수 있습니다 `('T1)` `(5)` `([1,2,3])` .
그러나 Q #은 singleton 튜플을 포함 된 형식의 값과 동일 하 게 처리 합니다.
즉,과 사이에 차이가 없으며,과 사이에 차이가 없습니다 `5` `(5)` `5` `(((5)))` `(5, (6))` `(5, 6)` .
작성 하는 것 처럼 작성 하는 것은 올바르지만 `(5)+3` `5+3` 두 식이 모두로 계산 됩니다 `8` .

이러한 동등성은 할당 및 식을 비롯 한 모든 용도에 적용 됩니다.
식이 지정 된 경우 괄호로 묶인 동일한 식이 동일한 형식의 식입니다.
예를 들어는 형식의 식이 고는 형식의 식이고는 `(7)` `Int` `([1,2,3])` `Int[]` `((1,2))` 형식의 식입니다 `(Int, Int)` .

특히이는 입력 튜플 또는 출력 튜플 형식에 단일 인수를 사용 하거나 단일 값을 반환 하는 하나의 필드가 있는 작업 또는 함수를 볼 수 있음을 의미 합니다.

이 속성은 _단일 튜플 동치_로 참조 됩니다.


## <a name="user-defined-types"></a>사용자 정의 형식

사용자 정의 형식 선언은 키워드로 구성 된 `newtype` 다음 사용자 정의 형식 이름, `=` , 유효한 형식 사양 및 종료 세미콜론으로 구성 됩니다.

예를 들면 다음과 같습니다.

```qsharp
newtype PairOfInts = (Int, Int);
```
    
* 각 Q # 소스 파일은 원하는 수의 사용자 정의 형식을 선언할 수 있습니다.
* 형식 이름은 네임 스페이스 내에서 고유 해야 하며 작업 및 함수 이름과 충돌 하지 않을 수 있습니다.
* 사용자 정의 형식은 기본 형식이 동일한 경우에도 고유 합니다.
특히 기본 형식이 동일한 경우에도 두 사용자 정의 형식의 값 사이에 자동 변환이 없습니다.

### <a name="named-vs-anonymous-items"></a>명명 된 항목과 익명 항목 비교

Q # 파일은 법적 형식의 단일 값을 포함 하는 새 명명 된 형식을 정의할 수 있습니다.
모든 튜플 형식의 경우 `T` 문을 사용 하 여의 하위 형식인 새 사용자 정의 형식을 선언할 수 있습니다 `T` `newtype` .
예를 들어 @"microsoft.quantum.math" 네임 스페이스에서 복소수는 사용자 정의 형식으로 정의 됩니다.

```qsharp
newtype Complex = (Double, Double);
```
이 문은 형식의 익명 항목 두 개를 사용 하 여 새 형식을 만듭니다 `Double` .   

익명 항목 외에도 사용자 정의 형식은 Q # 버전 0.7 이상으로 *명명 된 항목* 을 지원 합니다. 예를 들어 `Re` 복소수의 실수 부분을 나타내는 double에 대해 항목의 이름을로, 허수 부분에 대해로 이름을로 설정할 수 있습니다 `Im` . 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
사용자 정의 형식에서 한 항목의 이름을 지정 하는 것은 모든 항목의 이름을 지정 해야 한다는 의미는 아닙니다. 명명 된 항목 및 명명 되지 않은 항목의 모든 조합이 지원 됩니다. 또한 내부 항목의 이름을 지정할 수도 있습니다.
예를 들어 아래에 정의 된 형식에는 형식 `Nested` `(Double, (Int, String))` 의 항목만 이라는 기본 형식이 `Int` 있으며, 다른 모든 항목은 익명입니다. 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

명명 된 항목은 *액세스 연산자* 를 통해 직접 액세스할 수 있다는 장점이 있습니다 `::` . 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

잠재적으로 복잡 한 튜플 형식에 대 한 짧은 별칭을 제공 하는 것 외에도 이러한 형식을 정의 하면 특정 값의 의도를 문서화할 수 있습니다.
의 예제로 돌아가면 `Complex` 2d 극좌표 형 좌표를 사용자 정의 형식으로 정의 했을 수도 있습니다.

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

`Complex`와 `Polar` 둘 다 기본 형식이 있는 경우에도 `(Double, Double)` 두 형식이 모두 Q #에서 완전히 호환 되지 않으므로 극좌표를 사용 하 여 복잡 한 수학 함수를 실수로 호출 하는 위험을 최소화 하 고 그 반대의 경우도 마찬가지입니다.

#### <a name="access-anonymous-items-with-the-unwrap-operator"></a>래핑 해제 연산자를 사용 하 여 익명 항목 액세스

익명 항목에 액세스 하려면 먼저 후 위 연산자를 사용 하 여 래핑된 값을 추출 합니다 `!` .
"래핑 해제" 연산자를 사용 하 여 `!` 사용자 정의 형식에 포함 된 값을 추출할 수 있습니다.
이러한 "래핑 해제" 식의 형식은 사용자 정의 형식의 기본 형식입니다. 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

단일 래핑 해제 연산자는 한 줄의의 래핑을 해제 합니다. 여러 래핑 해제 연산자를 사용 하 여 곱하기 래핑된 값에 액세스 합니다.

예를 들면 다음과 같습니다.

```qsharp
newtype WrappedInt = Int;
newtype DoublyWrappedInt = WrappedInt;

...
    let x = DoublyWrappedInt(WrappedInt(6));
    let y = x!;       // y is WrappedInt(6)
    let z = x!!;      // z is 6
    let a = x + 5;    // This is an error, a DoublyWrappedInt isn't an Int
    let b = x! + 5;   // Also an error
    let c = x!! + 5;  // This is valid, c will be 11
...
```

래핑 해제 연산자에 대 한 자세한 내용은 [Q #의 형식 식](xref:microsoft.quantum.guide.expressions)을 참조 하세요.

### <a name="creating-values-of-user-defined-types"></a>사용자 정의 형식 값 만들기

해당 형식 생성자를 호출 하 여 사용자 정의 형식의 값을 만듭니다.

```qsharp
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

또는 [복사 및 업데이트 식을](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions)사용 하 여 기존 값에서 새 값을 만들 수 있습니다. 배열과 마찬가지로 복사 및 업데이트 식은 지정 된 명명 된 항목을 제외 하 고 원래 식의 모든 항목 값을 복사 합니다. 이러한 예외에 대해 이러한 항목의 값은 식의 오른쪽에 정의 된 값입니다. [업데이트 및 재할당 문과](xref:microsoft.quantum.guide.variables#update-and-reassign-statements)같이 배열 항목에 사용할 수 있는 다른 언어 구문은 사용자 정의 형식의 명명 된 항목에도 존재 합니다.

```qsharp
newtype ComplexArray = (Count : Int, Data : Complex[]);

function AsComplexArray (data : Double[]) : ComplexArray {

    mutable res = ComplexArray(0, new Complex[0]);
    for (item in data) {
        set res w/= Data <- res::Data + [Complex(item, 0.)]; // update-and-reassign statement
    }
    return res w/ Count <- Length(res::Data); // returning a copy-and-update expression
}
```

* 다른 형식을 사용 하는 모든 위치에서 사용자 정의 형식을 사용할 수 있습니다.
특히 사용자 정의 형식의 배열을 정의 하 고 사용자 정의 형식을 튜플 형식의 요소로 포함 하는 것이 가능 합니다.

* 재귀 형식 구조를 만들 수는 없습니다.
즉, 사용자 정의 형식을 정의 하는 형식은 사용자 정의 형식의 요소를 포함 하는 튜플 형식일 수 없습니다.
보다 일반적으로 사용자 정의 형식에는 순환 종속성이 있을 수 없으므로 다음과 같은 형식 정의 집합이 잘못 되었습니다.

    ```qsharp
    newtype TypeA = (Int, TypeB);
    newtype TypeB = (Double, TypeC);
    newtype TypeC = (TypeA, Range);
    ```


## <a name="operation-and-function-types"></a>작업 및 함수 형식

다음 형식 및이 제공 됩니다 `'Tinput` `'Tresult` .

* `('Tinput => 'Tresult)`는 모든 *작업*(예:)에 대 한 기본 형식입니다 `((Qubit, Pauli) => Result)` .
* `('Tinput -> 'Tresult)`는 *함수*에 대 한 기본 형식입니다 (예:) `(Int -> Int)` . 

이를 호출 가능의 *서명* 이라고 합니다.

* 모든 Q # callables은 단일 값을 입력으로 사용 하 고 단일 값을 출력으로 반환 합니다.
* 입력 및 출력 값 모두에 튜플을 사용할 수 있습니다.
* 결과가 없는 callables은을 반환 `Unit` 합니다.
* 입력이 없는 callables은 빈 튜플을 입력으로 사용 합니다.

### <a name="functors"></a>함수

*함수* 형식은 해당 시그니처로 완전히 지정 됩니다. 예를 들어, 각도의 사인을 계산 하는 함수는 형식을 갖습니다 `(Double -> Double)` . 

작업에는 작업 형식의 일부로 표시 되는 특정 추가 *특징이 있습니다.* 이러한 특성에는 작업에서 지 원하는 *함수* 에 대 한 정보가 포함 됩니다.
예를 들어 작업 실행이 다른 비트의 상태를 사용 하는 경우 함수를 지원 해야 합니다 `Controlled` . 작업에 역이 있으면 함수를 지원 해야 합니다 `Adjoint` .

> [!NOTE]
> 이 문서에서는 함수에서 작업 서명을 변경 하는 방법에 대해서만 설명 합니다. 함수 및 작업에 대 한 자세한 내용은 [Q #의 작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions)를 참조 하세요. 

`Controlled`작업 형식에서 and/or 함수를 지원 하려면 `Adjoint` 해당 특성을 나타내는 주석을 추가 해야 합니다.
주석 `is Ctl` (예:)은 `(Qubit => Unit is Ctl)` 작업을 제어할 수 있음을 나타냅니다. 즉, 실행은 다른의 상태를 사용 합니다. 마찬가지로 주석은 `is Adj` 작업에 adjoint가 있음을 나타냅니다. 즉, 작업을 연속적으로 적용 한 다음 해당 adjoint 상태를 변경 되지 않은 상태로 유지 하는 "반전" 될 수 있습니다. 

해당 형식의 작업에서 및 함수를 둘 다 지원 하도록 요구 하려는 경우 `Adjoint` `Controlled` 이를로 표현할 수 있습니다 `(Qubit => Unit is Adj + Ctl)` . 예를 들어 기본 제공 Pauli 작업에는 <xref:microsoft.quantum.intrinsic.x> 형식이 `(Qubit => Unit is Adj + Ctl)` 있습니다. 

함수을 지원 하지 않는 작업 형식은 입력 및 출력 형식 만으로 지정 되 고 추가 주석은 포함 하지 않습니다.

### <a name="type-parameterized-functions-and-operations"></a>형식 매개 변수화 된 함수 및 작업

호출 가능 형식에는 *형식 매개 변수가*포함 될 수 있습니다.
작은따옴표를 접두사로 사용 하는 기호를 사용 하 여 형식 매개 변수를 나타냅니다. 예를 들어 `'A` 은 올바른 형식 매개 변수입니다.
형식 매개 변수화 된 callables을 정의 하는 방법에 대 한 자세한 내용 및 자세한 내용은 [Q #의 작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables)를 참조 하세요.

단일 서명에서 형식 매개 변수가 두 번 이상 나타날 수 있습니다.
예를 들어, 배열의 각 요소에 다른 함수를 적용 하 고 수집 된 결과에 시그니처가 있음을 반환 하는 함수입니다 `(('A[], 'A->'A) -> 'A[])` .
마찬가지로 두 작업의 컴퍼지션을 반환 하는 함수에는 시그니처가 `((('A=>'B), ('B=>'C)) -> ('A=>'C))` 있습니다.

형식이 매개 변수가 있는 호출 가능 매개 변수를 호출 하는 경우 동일한 형식 매개 변수를 갖는 모든 인수는 동일한 형식 이어야 합니다.

Q #은 사용자가 형식 매개 변수를 대체할 수 있는 가능한 형식을 제한 하는 메커니즘을 제공 하지 않습니다.

## <a name="next-steps"></a>다음 단계

Q # 언어를 구성 하는 모든 형식을 살펴보았으므로 이제 이러한 다양 한 형식의 식을 만들고 조작 하는 방법을 알아보려면 [q #의 형식 식](xref:microsoft.quantum.guide.expressions) 을 참조 하세요.
