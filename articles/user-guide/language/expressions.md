---
title: 'Q의 형식 식 #'
description: 'Q #에서 상수, 변수, 연산자, 작업 및 함수를 식으로 지정, 참조 및 결합 하는 방법을 이해 합니다.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
ms.openlocfilehash: c4b2cc0bed44ffdfb191ba522d6526959e7c6708
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327308"
---
# <a name="type-expressions-in-q"></a>Q의 형식 식 #

## <a name="numeric-expressions"></a>숫자 식

숫자 식은, 또는 형식의 식 `Int` 입니다 `BigInt` `Double` .
즉, 정수 또는 부동 소수점 숫자 중 하나입니다.

`Int`Q #의 리터럴은 단순히 숫자 시퀀스로 작성 됩니다.
16 진수 및 이진 정수는 `0x` 각각 및 접두사를 사용 하 여 지원 됩니다 `0b` .

`BigInt`Q #의 리터럴은 후행 또는 접미사로 작성 됩니다 `l` `L` .
16 진수 큰 정수는 "0x" 접두사를 사용 하 여 지원 됩니다.
따라서 다음은 리터럴의 모든 유효한 사용입니다 `BigInt` .

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

`Double`Q #의 리터럴은 10 진수를 사용 하 여 작성 된 부동 소수점 숫자입니다.
소수점, `.` 및/또는 ' e ' 또는 ' e '로 표시 된 지 수 부분을 사용 하 여 작성할 수 있습니다 .이 경우에는 가능한 음수 부호와 소수 자릿수만 유효 합니다.
유효한 `Double` 리터럴은 `0.0` , `1.2e5` , `1e-5` 입니다.

모든 요소 형식의 배열 식이 지정 된 경우 `Int` 기본 제공 함수를 사용 하 여 식을 구성 하 [`Length`](xref:microsoft.quantum.core.length) 고, 배열 식이 괄호로 묶여 있으며,를 사용 하 여 식을 만들 수 있습니다 `(` `)` .
예를 들어 `a` 가 배열에 바인딩된 경우 `Length(a)` 는 정수 식입니다.
`b`가 정수 배열의 배열인 경우는 `Int[][]` `Length(b)` 의 하위 배열 수이 `b` 고 `Length(b[1])` 은의 두 번째 하위 배열에 있는 정수 수입니다 `b` .

동일한 형식의 두 숫자 식이 지정 된 경우 이항 연산자 `+` , `-` , 및를 `*` `/` 사용 하 여 새 숫자 식을 만들 수 있습니다.
새 식의 형식은 구성 식의 형식과 동일 합니다.

두 개의 정수 식이 지정 되 면 이항 연산자 `^` (power)를 사용 하 여 새 정수 식을 만들 수 있습니다.
마찬가지로를 `^` 두 개의 double 식과 함께 사용 하 여 새 double 식을 만들 수 있습니다.
마지막으로,은 `^` 왼쪽에서 큰 정수를 사용 하 고 오른쪽에는 정수를 사용 하 여 새 큰 정수 식을 만들 수 있습니다.
이 경우 두 번째 매개 변수는 32 비트에 맞아야 합니다. 그렇지 않으면 런타임 오류가 발생 합니다.

두 개의 정수 또는 큰 정수 식이 지정 된 경우 `%` (모듈러스), `&&&` (비트 and), (비트 or `|||` ) 또는 `^^^` (비트 XOR) 연산자를 사용 하 여 새 정수 또는 큰 정수 식의 형식을 지정할 수 있습니다.

왼쪽에 정수 또는 큰 정수 식이 있고 오른쪽에 정수 식이 지정 된 경우 `<<<` (산술 왼쪽 시프트) 또는 `>>>` (산술 오른쪽 시프트) 연산자를 사용 하 여 왼쪽 식과 동일한 형식의 새 식을 만들 수 있습니다.

이동 작업에 대 한 두 번째 매개 변수 (이동 크기)는 0 보다 크거나 같아야 합니다. 음수 시프트 금액의 동작은 정의 되지 않습니다.
시프트 연산의 이동 양은 32 비트에도 맞아야 합니다. 그렇지 않으면 런타임 오류가 발생 합니다.
이동할 숫자가 정수 이면 시프트 금액이 해석 됩니다 `mod 64` . 즉, 1의 시프트와 65의 시프트는 동일한 효과를 가집니다.

정수 및 큰 정수 값 모두에 대해 시프트는 산술 연산입니다.
음수 값을 왼쪽 이나 오른쪽으로 이동 하면 음수가 반환 됩니다.
즉, 한 단계를 왼쪽 또는 오른쪽으로 이동 하는 것은 각각 2로의 곱하기 또는 나누기와 정확히 동일 합니다.

정수 나누기와 정수 모듈러스는 c #과 같은 음수에 대해 동일한 동작을 수행 합니다.
즉,는 `a % b` 항상와 동일한 기호를 가집니다 .이는 항상와 동일 `a` `b * (a / b) + a % b` `a` 합니다.
예를 들면 다음과 같습니다.

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 5 | 2 | 2 | 1
 5 | -2 | -2 | 1
 -5 | 2 | -2 | -1
 -5 | -2 | 2 | -1

큰 정수 나누기와 모듈러스는 동일한 방식으로 작동 합니다.

숫자 식이 지정 된 경우 단항 연산자를 사용 하 여 새 식을 지정할 수 있습니다 `-` .
새 식은 구성 식과 동일한 형식이 됩니다.

정수 또는 큰 정수 식이 지정 된 경우 `~~~` (비트 보수) 단항 연산자를 사용 하 여 동일한 유형의 새 식을 설정할 수 있습니다.

## <a name="boolean-expressions"></a>부울 식

두 `Bool` 리터럴 값은 `true` 및 `false` 입니다.

동일한 기본 형식의 두 식이 지정 된 경우 `==` 및 `!=` 이항 연산자를 사용 하 여 식을 생성할 수 있습니다 `Bool` .
식은 두 식이 같으면 true이 고, 그렇지 않으면 false입니다.

사용자 정의 형식의 값을 비교할 수 없습니다. 래핑 해제 된 값만 비교할 수 있습니다. 예를 들어 "래핑 해제" 연산자 `!` ( [Q #의 형식](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)에 자세히 설명 되어 있음)를 사용 합니다.

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

값에 대 한 같음 비교 `Qubit` 는 id 같음입니다. 즉, 두 식이 동일한의 비트를 식별 하는지 여부입니다.
이 비교로 두 비트의 상태를 비교, 액세스, 측정 또는 수정할 수 없습니다.

반올림 결과 때문에 값에 대 한 같음 비교가 `Double` 잘못 될 수 있습니다.
예를 들면 `49.0 * (1.0/49.0) != 1.0` 입니다.

두 숫자 식이 지정 된 경우 이항 연산자 `>` , `<` , 및를 `>=` `<=` 사용 하 여 첫 번째 식이 두 번째 식 보다 크거나 같고 보다 작거나 같은 경우 true 인 새 부울 식을 생성할 수 있습니다.

부울 식을 두 개 지정 하는 `and` `or` 경우 및 이항 연산자를 사용 하 여 두 식 중 하나 (응답 또는 둘 다)가 true 인 경우 true 인 새 부울 식을 생성할 수 있습니다.

부울 식이 지정 된 `not` 경우 단항 연산자를 사용 하 여 구성 식이 false 인 경우 true 인 새 부울 식을 생성할 수 있습니다.

## <a name="string-expressions"></a>문자열 식

Q #에서는 문에 사용 되는 문자열 `fail` ( [제어 흐름](xref:microsoft.quantum.guide.controlflow#fail-statement)에 설명)과 표준 함수를 사용할 수 있습니다 [`Message`](xref:microsoft.quantum.intrinsic.message) .
후자의 특정 동작은 사용 되는 시뮬레이터에 따라 다르지만 일반적으로 Q # 프로그램을 실행 하는 동안 호출 될 때 호스트 콘솔에 메시지를 기록 합니다.

Q #의 문자열은 리터럴 또는 보간된 문자열입니다.

문자열 리터럴은 대부분의 언어에서 간단한 문자열 리터럴과 유사 합니다. 큰따옴표 안의 유니코드 문자 시퀀스 `"` 입니다.
문자열 내에서 백슬래시 문자를 사용 하 여 `\` 큰따옴표 문자를 이스케이프 하 고 새 줄을로 `\n` , 캐리지 리턴을로 `\r` , 탭을로 삽입할 수 있습니다 `\t` .
예를 들면 다음과 같습니다.

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a>보간된 문자열

문자열 보간에 대 한 Q # 구문은 c # 구문의 하위 집합 이지만 여기서는 Q #와 관련 된 주요 요점을 요약 합니다.
주요 차이점은 아래에 설명 되어 있습니다.

문자열 리터럴을 보간된 문자열로 식별하려면 `$` 기호를 사용하여 추가합니다.
`$` `"` 문자열과 문자열 리터럴을 시작 하는 사이에는 공백을 사용할 수 없습니다.

다음은 함수를 사용 하 여 [`Message`](xref:microsoft.quantum.intrinsic.message) 다른 Q # 식과 함께 측정 결과를 콘솔에 쓰는 기본적인 예입니다.

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```
유효한 Q # 식은 보간된 문자열에 나타날 수 있습니다.

C # 구문에 대 한 자세한 내용은 [*보간된 문자열*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings)에서 찾을 수 있습니다.
가장 주목할 만한 차이점은 Q #은 축 자 (여러 줄) 보간된 문자열을 지원 하지 않는다는 것입니다.
보간된 문자열 내부의 식은 c # 구문이 아니라 Q # 구문을 따릅니다.

## <a name="range-expressions"></a>범위 식

3 개의 식, 및가 지정 된 경우이 `Int` `start` `step` `stop` `start .. step .. stop` `start` `start+step` `start+step+step` 전달 될 때까지 첫 번째 요소가이 고, 두 번째 요소가 `stop` 이 고, 세 번째 요소가 인 범위 식입니다.
예를 들어,가 양수인 경우 범위는 비어 있을 수 있습니다 `step` `stop < start` .
범위의 마지막 요소는 `stop` 와의 차이가의 정수 배수가 면가 `start` 됩니다 `stop` `step` . 즉, 범위는 양쪽 끝에 포함 됩니다.

두 식 및가 지정 된 경우는와 `Int` `start` `stop` `start .. stop` 같은 범위 식입니다 `start .. 1 .. stop` .
`step`가 보다 작은 경우에도 암시는 + 1입니다 .이 `stop` `start` 경우 범위는 비어 있습니다.

몇 가지 예제 범위는 다음과 같습니다.

- `1..3`은 1, 2, 3의 범위입니다.
- `2..2..5`는 범위 2, 4입니다.
- `2..2..6`는 2, 4, 6 범위입니다.
- `6..-2..2`는 6, 4, 2 범위입니다.
- `2..1`는 빈 범위입니다.
- `2..6..7`는 범위 2입니다.
- `2..2..1`는 빈 범위입니다.
- `1..-1..2`는 빈 범위입니다.

## <a name="qubit-expressions"></a>Bit 식

유일한 `Qubit` 식은 `Qubit` 배열의 배열 요소 또는 값에 바인딩되는 기호입니다 `Qubit` .
`Qubit`리터럴이 없습니다.

## <a name="pauli-expressions"></a>Pauli 식

,, 및의 네 가지 `Pauli` 값은 `PauliI` `PauliX` `PauliY` `PauliZ` 모두 유효한 `Pauli` 식입니다.

그 외에도 유일한 `Pauli` 식은 `Pauli` 배열의 배열 요소 또는 값에 바인딩되는 기호입니다 `Pauli` .

## <a name="result-expressions"></a>결과 식

두 `Result` 값 및는 `One` `Zero` 유효한 `Result` 식입니다.

그 외에도 유일한 `Result` 식은 `Result` 배열의 배열 요소 또는 값에 바인딩되는 기호입니다 `Result` .
특히는 `One` 정수와 동일 하지 않으며 `1` 두 요소 사이에 직접 변환 되지 않습니다.
및의 경우에도 마찬가지입니다 `Zero` `0` .

## <a name="tuple-expressions"></a>튜플 식

튜플 리터럴은 및로 묶인 적절 한 형식의 요소 식 시퀀스로, 쉼표로 구분 됩니다 `(` `)` .
예를 들어 `(1, One)` 은 `(Int, Result)` 식입니다.

리터럴 이외의 튜플 식은 튜플 값에 바인딩된 기호, 튜플 배열의 배열 요소 및 튜플을 반환 하는 호출 가능 호출입니다.

## <a name="user-defined-type-expressions"></a>사용자 정의 형식 식

사용자 정의 형식의 리터럴은 형식 이름과 해당 형식의 기본 튜플 형식의 튜플 리터럴로 구성 됩니다.
예를 들어, `IntPair` 가를 기반으로 하는 사용자 정의 형식인 경우 `(Int, Int)` `IntPair(2, 3)` 는 해당 형식의 유효한 리터럴입니다.

리터럴 외에 사용자 정의 형식의 유일한 식은 해당 형식의 값에 바인딩된 기호, 해당 형식의 배열 요소, 해당 형식을 반환 하는 호출 가능 호출입니다.

## <a name="unwrap-expressions"></a>래핑 해제 식

Q #에서 래핑 해제 연산자는 후행 감탄 부호 `!` 입니다.
예를 들어, `IntPair` 가 기본 형식의 사용자 정의 형식이 `(Int, Int)` 고 `s` 값이 인 변수인 경우는 `IntPair(2, 3)` `s!` `(2, 3)` 입니다.

사용자 정의 형식에 대해 정의 합니다. 래핑 해제 연산자는 반복 될 수 있습니다. 예를 들어는 `s!!` 이중 래핑 해제 된 값을 `s` 나타냅니다.
따라서 `WrappedPair` 가 기본 형식의 사용자 정의 형식이 `IntPair` 고 `t` 가 값이 포함 된 변수인 경우은 `WrappedPair(IntPair(1,2))` `t!!` `(1,2)` 입니다.

`!`연산자는 `[]` 배열 인덱싱 및 조각화를 위해 이외의 다른 모든 연산자 보다 우선 순위가 높습니다.
`!`및 `[]` bind 메서드에 액세스할. 즉, `a[i]![3]` `((a[i])!)[3]` `i` 의 ' 번째 요소를 가져와 래핑 해제 한 `a` 다음 래핑 해제 된 값 (배열 이어야 함)의 세 번째 요소를 가져옵니다.

연산자의 우선 순위에는 `!` 명확 하지 않을 수 있는 영향이 하나 있습니다.
함수 또는 작업에서 래핑 해제 되는 값을 반환 하는 경우 인수 튜플이 래핑 되지 않고 호출에 바인딩되도록 함수 또는 작업 호출을 괄호로 묶어야 합니다.
예를 들면 다음과 같습니다.

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a>배열 식

배열 리터럴은 및로 묶인 하나 이상의 요소 식의 시퀀스로, 쉼표로 구분 됩니다 `[` `]` .
모든 요소는 동일한 형식과 호환 되어야 합니다.

동일한 형식의 두 배열이 지정 된 경우 이항 연산자를 `+` 사용 하 여 두 배열의 연결 인 새 배열을 만들 수 있습니다.
예를 들어 `[1,2,3] + [4,5,6]` 은 `[1,2,3,4,5,6]` 입니다.

### <a name="array-creation"></a>배열 만들기

형식 및 식이 지정 된 경우 `Int` 연산자를 `new` 사용 하 여 지정 된 크기의 새 배열을 할당할 수 있습니다.
예를 들어는 `new Int[i + 1]` `Int` 요소로 새 배열을 할당 `i + 1` 합니다.

빈 배열 리터럴는 `[]` 허용 되지 않습니다.
대신를 사용 하는 대신를 사용 합니다 `new ★[0]` `★` . 여기서은 적절 한 형식에 대 한 자리 표시자입니다 .를 사용 하면 원하는 길이 0 배열을 만들 수 있습니다

새 배열의 요소는 형식 종속 기본값으로 초기화 됩니다.
대부분의 경우이 값은 0으로 변형 된 것입니다.

엔터티를 참조 하는 callables 및 callables의 경우 적절 한 기본값이 없습니다.
따라서 이러한 형식의 경우 기본값은 런타임 오류를 발생 시 키 지 않고 사용할 수 없는 잘못 된 참조입니다.
이는 c #, Java 등의 언어에서 null 참조와 비슷합니다.
요소가 안전 하 게 사용 되기 전에는 기본값이 아닌 값을 사용 하 여 valbits 또는 callables을 포함 하는 배열을 적절 하 게 초기화 해야 합니다. 적절 한 초기화 루틴은에서 찾을 수 있습니다 <xref:microsoft.quantum.arrays> .

각 형식에 대 한 기본값은 다음과 같습니다.

Type | 기본값
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | _invalid qubit_
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | 빈 범위`1..1..0`
 `Callable` | _invalid callable_
 `Array['T]` | `'T[0]`

튜플 형식은 요소에 의해 초기화 됩니다.


### <a name="array-elements"></a>배열 요소

배열 식과 식이 지정 된 경우 `Int` `[` 및 `]` 배열 요소 연산자를 사용 하 여 새 식을 설정할 수 있습니다.
새 식은 배열의 요소 형식과 동일한 형식이 됩니다.
예를 들어, `a` 가 s의 배열에 바인딩되면은 `Double` 식입니다 `a[4]` `Double` .

배열 식이 단순 식별자가 아니면 요소를 선택 하기 위해 괄호로 묶어야 합니다.
예를 들어 `a` 및 `b` 가 모두 s의 배열인 경우 `Int` 연결의 요소가 다음과 같이 표시 됩니다.

```qsharp
(a + b)[13]
```

Q #의 모든 배열은 0부터 시작 합니다.
즉, 배열의 첫 번째 요소는 `a` 항상 `a[0]` 입니다.


### <a name="array-slices"></a>배열 조각

배열 식과 식이 지정 된 경우 `Range` `[` 및 `]` 배열 조각 연산자를 사용 하 여 새 식을 설정할 수 있습니다.
새 식은 배열과 동일한 형식이 되며의 요소에 의해 인덱싱된 배열 항목이 `Range` 에 정의 된 순서 대로 포함 됩니다 `Range` .
예를 들어, `a` 가 s의 배열에 바인딩된 경우는 `Double` `a[3..-1..0]` `Double[]` 의 처음 4 개 요소를 포함 `a` 하지만에 표시 되는 역순으로를 포함 하는 식입니다 `a` .

`Range`이 비어 있으면 결과 배열 조각의 길이가 0이 됩니다.

참조 하는 배열 요소와 마찬가지로, 배열 식이 단순 식별자가 아니면 조각화 하기 위해 괄호로 묶어야 합니다.
`a`및 `b` 가 모두 s 배열인 경우 `Int` 연결의 조각이 다음과 같이 표시 됩니다.

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a>유추 된 시작/끝 값

0.8 릴리스부터는 범위 조각화를 위한 상황별 식을 지원 합니다. 특히 범위 분할 식의 컨텍스트에서는 범위 시작 값과 끝 값을 생략할 수 있습니다. 이 경우 컴파일러는 범위에 대해 의도 된 구분 기호를 유추 하기 위해 다음 규칙을 적용 합니다. 

예를 들어 range start 값을 생략 하면 유추 된 시작 값이 
- 지정 된 단계가 없거나 지정 된 단계가 양수 이면 0이 고, 그렇지 않으면입니다. 
- 지정 된 단계가 음수인 경우 분리 된 배열의 길이에서 1을 뺀 값입니다. 

범위 끝 값이 생략 된 경우에는 유추 된 끝 값이 
- 지정 된 단계가 없고 지정 된 단계가 양수인 경우 분리 된 배열의 길이가 1을 뺀 값입니다. 
- 지정 된 단계가 음수 이면 0이 반환 됩니다. 

```qsharp
let arr = [1,2,3,4,5,6];
let slice1  = arr[3...];      // slice1 is [4,5,6];
let slice2  = arr[0..2...];   // slice2 is [1,3,5];
let slice3  = arr[...2];      // slice3 is [1,2,3];
let slice4  = arr[...2..3];   // slice4 is [1,3];
let slice5  = arr[...2...];   // slice5 is [1,3,5];
let slice7  = arr[4..-2...];  // slice7 is [5,3,1];
let slice8  = arr[...-1..3];  // slice8 is [6,5,4];
let slice9  = arr[...-1...];  // slice9 is [6,5,4,3,2,1];
let slice10 = arr[...];       // slice10 is [1,2,3,4,5,6];
```

### <a name="copy-and-update-expressions"></a>복사 및 업데이트 식

모든 Q # 형식은 값 형식이 며,이는 모든 것이 특별 한 역할을 수행 하기 때문에 값이 기호에 바인딩되거나 기호가 바인딩 되었을 때 "copy"가 생성 됩니다. 즉, Q #의 동작은 할당 시 복사본이 생성 된 경우와 동일 합니다.
물론 관련 된 부분만 실제로 필요에 따라 다시 생성 됩니다. 

특히 배열도 포함 됩니다.
특히 배열 항목을 업데이트할 수 없습니다. 기존 배열을 수정 하려면 *복사 및 업데이트* 메커니즘을 활용 해야 합니다.

기존 배열에서 *복사 및 업데이트* 식을 통해 새 배열을 만들 수 있습니다.
복사 및 업데이트 식은 형식의 식이 며 `expression1 w/ expression2 <- expression3` , 여기서은 `expression1` `T[]` 특정 형식의 형식 이어야 `T` 합니다.
두 번째는 `expression2` 에서 배열과 비교 하 여 수정할 요소의 인덱스를 정의 하 고, 형식 또는 형식 중 `expression1` 하나 여야 `Int` `Range` 합니다.
`expression2`가 형식이 면은 `Int` `expression3` 형식 이어야 `T` 합니다. `expression2`가 형식이 면은 `Range` `expression3` 형식 이어야 `T[]` 합니다.

복사 및 업데이트 식은의 `arr w/ idx <- value` 해당 요소로 설정 된 모든 요소를 포함 하는 새 배열을 생성 합니다 .이 요소는의 요소를 제외 하 고는의 해당 요소로 `arr` `idx` 설정 됩니다 `value` . 예를 들어에 `arr` 배열이 포함 된 `[0,1,2,3]` 경우 
- `arr w/ 0 <- 10`는 배열 `[10,1,2,3]` 입니다.
- `arr w/ 2 <- 10`는 배열 `[0,1,10,3]` 입니다.
- `arr w/ 0..2..3 <- [10,12]`는 배열 `[10,1,12,3]` 입니다.

#### <a name="copy-and-update-expressions-for-named-items"></a>명명 된 항목에 대 한 복사 및 업데이트 식

사용자 정의 형식에 명명 된 항목에 대 한 유사한 식이 있습니다. 

예를 들어 형식 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
에 `c` 형식의 값이 포함 된 경우 `Complex(1., -1.)` `c w/ Re <- 0.` 는 `Complex` 로 계산 되는 형식의 식입니다 `Complex(0., -1.)` .

### <a name="jagged-arrays"></a>가변 배열

"배열의 배열"이 라고도 하는 가변 배열은 요소가 배열인 배열입니다.
가변 배열의 요소는 크기가 다를 수 있습니다.
다음 예에서는 곱하기 테이블을 나타내는 가변 배열을 선언 하 고 초기화 하는 방법을 보여 줍니다.

```qsharp
let N = 4;
mutable multiplicationTable = new Int[][N];
for (i in 1..N) {
    mutable row = new Int[i];
    for (j in 1..i) {
        set row w/= j-1 <- i * j;
    }
    set multiplicationTable w/= i-1 <- row;
}
```

### <a name="arrays-of-callables"></a>Callables 배열 

호출 가능 형식에 대 한 자세한 내용은 다음 페이지, [Q #의 작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions)에 나와 있습니다.

공통 요소 형식이 작업 또는 함수 형식이 면 모든 요소에 동일한 입력 및 출력 형식이 있어야 합니다.
배열의 요소 형식은 모든 요소에서 지원 되는 모든 함수을 지원 합니다.
예를 들어, `Op1` `Op2` 및 `Op3` 모두가 이지만,를 `Qubit[] => Unit` `Op1` 지원 하 `Adjoint` `Op2` `Controlled` 고 `Op3` 를 지원 하며를 지원 합니다.

- `[Op1, Op2]`는 작업의 배열입니다 `(Qubit[] => Unit)` .
- `[Op1, Op3]`는 작업의 배열입니다 `(Qubit[] => Unit is Adj)` .
- `[Op2, Op3]`는 작업의 배열입니다 `(Qubit[] => Unit is Ctl)` .

그러나 `(Qubit[] => Unit is Adj)` 및 `(Qubit[] => Unit is Ctl)` 작업의 공통 기본 형식은 이지만 `(Qubit[] => Unit)` 이러한 연산자 *의* 배열은 공통 기본 형식을 공유 하지 않습니다. 예를 들어는 `[[Op1], [Op2]]` 호환 되지 않는 배열 형식 및의 배열을 만들려고 하기 때문에 현재 오류를 발생 시킵니다 `(Qubit[] => Unit is Adj)[]` `(Qubit[] => Unit is Ctl)[]` .


## <a name="conditional-expressions"></a>조건 식

동일한 형식 및 부울 식의 다른 두 식이 지정 된 경우 물음표 및 세로 막대를 사용 하 여 조건 식을 지정할 수 있습니다 `?` `|` .
예를 들면 `a==b ? c | d` 입니다.
이 예에서는 조건식의 값이 true 이면이 고, `c` 그렇지 `a==b` `d` 않으면 false입니다.

### <a name="conditional-expressions-with-callables"></a>Callables 사용 조건 식

두 식은 동일한 입력 및 출력을 포함 하는 작업으로 평가 될 수 있지만 다른 함수을 지원 합니다.
이 경우 조건식의 형식은 두 식에서 지원 되는 모든 함수를 지 원하는 입력 및 출력을 사용 하는 작업입니다.
예를 들어, `Op1` `Op2` 및 `Op3` 모두가 이지만,를 `Qubit[]=>Unit` `Op1` 지원 하 `Adjoint` `Op2` `Controlled` 고 `Op3` 를 지원 하며를 지원 합니다.

- `flag ? Op1 | Op2`은 `(Qubit[] => Unit)` 작업입니다.
- `flag ? Op1 | Op3`은 `(Qubit[] => Unit is Adj)` 작업입니다.
- `flag ? Op2 | Op3`은 `(Qubit[] => Unit is Ctl)` 작업입니다.

가능한 두 결과 식 중 하나에 함수 또는 작업 호출이 포함 된 경우 해당 호출은 호출의 값이 되는 경우에만 수행 됩니다.
예를 들어, `a==b ? C(qs) | D(qs)` `a==b` 이 true 이면 `C` 작업이 호출 되 고 false 인 경우에만 `D` 호출 됩니다.
이는 다른 언어의 단락과 비슷합니다.

## <a name="callable-expressions"></a>호출 가능 식

호출 가능 리터럴은 컴파일 범위에서 정의 된 작업 또는 함수의 이름입니다.
예를 들어 `X` 는 표준 라이브러리 작업을 참조 하는 작업 리터럴이어야,는 `X` `Message` 표준 라이브러리 함수를 참조 하는 함수 리터럴입니다 `Message` .

작업에서 함수를 지 원하는 경우 `Adjoint` `Adjoint op` 는 연산 식입니다.
마찬가지로 작업에서 함수를 지 원하는 경우 `Controlled` `Controlled op` 는 연산 식입니다.
이러한 식의 형식은 [작업 특수화 호출](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations)시 지정 됩니다.

함수 ( `Adjoint` 및 `Controlled` )은 `!` [] '로 래핑 연산자 및 배열 인덱싱을 제외 하 고 다른 모든 연산자 보다 더 가깝게 바인딩합니다.
따라서 다음은 작업에서 사용 되는 함수를 지원 한다고 가정 하 여 모든 법률입니다.

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a>형식 매개 변수가 있는 호출 가능 식

호출 가능 리터럴은 값으로 사용 될 수 있습니다. 예를 들어 변수에 할당 하거나 다른 호출 가능으로 전달 합니다.
이 경우 호출 가능에 [형식 매개 변수가 있으면 해당 매개 변수](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables)를 호출 가능 값의 일부로 제공 해야 합니다.
호출 가능 값은 지정 되지 않은 형식 매개 변수를 가질 수 없습니다.

예를 들어 `Fun` 가 시그니처를 사용 하는 함수인 경우는 `'T1->Unit` 다음과 같습니다.

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a>호출 가능 호출 식

호출 가능 식의 입력 형식에 대 한 호출 가능 (연산 또는 함수) 식과 튜플 식이 지정 된 경우 호출 식은 튜플 식을 호출 가능 식에 추가 하 여 구성 될 수 있습니다.
호출 식의 형식은 호출 가능 시그니처의 출력 형식입니다.

예를 들어 `Op` 가 서명이 포함 된 작업 인 `((Int, Qubit) => Double)` 경우 `Op(3, qubit1)` 는 형식의 식입니다 `Double` .
마찬가지로 `Sin` 가 시그니처를 사용 하는 함수인 `(Double -> Double)` 경우 `Sin(0.1)` 는 형식의 식입니다 `Double` .
마지막으로 `Builder` 가 시그니처를 사용 하는 함수인 경우 `(Int -> (Int -> Int))` `Builder(3)` 는에서 Int로의 함수입니다.

호출 가능 값 식의 결과를 호출 하려면 호출 가능 식 주위에 괄호 쌍을 추가 해야 합니다.
따라서 이전 단락에서 호출 결과를 호출 하려면 `Builder` 올바른 구문은 다음과 같습니다.

```qsharp
(Builder(3))(2)
```

[형식 매개 변수가 있는](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) 호출 가능를 호출할 때 실제 형식 매개 변수는 꺾쇠 괄호 내에서 `<` `>` 호출 가능 식 뒤에 지정할 수 있습니다.
이는 일반적으로 Q # 컴파일러가 실제 형식을 유추 하므로 필요 하지 않습니다.
그러나 형식 매개 변수가 있는 인수를 지정 하지 *않은 상태로 두면* [부분 응용 프로그램](xref:microsoft.quantum.guide.operationsfunctions#partial-application) 에 필요 합니다.
또한 다른 함수를 사용 하는 작업을 호출할 수 있는 경우에도 유용 합니다.

예를 들어,에 시그니처가 있고,에 시그니처가 있고,가 첫 번째 인수로를 사용 하 여를 호출 하 고,를 `Func` `('T1, 'T2, 'T1) -> 'T2` 세 번째 `Op1` `Op2` `(Qubit[] => Unit is Adj)` `Op3` `(Qubit[] => Unit)` 인수로 호출 하는 시그니처가 `Func` `Op1` `Op2` `Op3` 있는 경우입니다.

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

및에 다른 형식이 있으므로 형식 사양이 필요 합니다 `Op3` `Op1` . 따라서 컴파일러는 사양을 사용 하지 않고이를 모호 하 게 처리 합니다.


## <a name="operator-precedence"></a>연산자 우선 순위

모든 이항 연산자는를 제외 하 고 오른쪽 결합성이 `^` 있습니다.

대괄호 및 `[` 는 `]` 배열 조각화 및 인덱싱의 경우 모든 연산자 앞에 바인딩합니다.

함수 `Adjoint` 및는 `Controlled` 배열 인덱싱 후 다른 모든 연산자 앞에 바인딩합니다.

연산 및 함수 호출에 대 한 괄호는 모든 연산자 앞에, 배열 인덱싱 및 함수 후에도 바인딩됩니다.

우선 순위 순으로 최고에서 최저 순으로 연산자.

연산자 | 숫자 | 설명 | 피연산자 형식
---------|----------|---------|---------------
 붙이지`!` | 단항 연산자 | 래핑 취소 | 사용자 정의 형식
 `-`, `~~~`, `not` | 단항 연산자 | 숫자 음수, 비트 보수, 논리 부정 | `Int`,의 경우,,의 경우,의 경우 `BigInt` `Double` `-` `Int` `BigInt` `~~~` `Bool``not`
 `^` | 이진 | 정수 거듭제곱 | `Int`또는 기준의 경우 지 수의 경우입니다. `BigInt` `Int`
 `/`, `*`, `%` | 이진 | 나누기, 곱하기, 정수 모듈러스 | `Int`,,, 또는 `BigInt` `Double` `/` `*` `Int` `BigInt` 의 경우`%`
 `+`, `-` | 이진 | 더하기 또는 문자열 및 배열 연결, 빼기 | `Int`,, `BigInt` 또는 `Double` `String` 에 대 한 배열 형식입니다.`+`
 `<<<`, `>>>` | 이진 | 왼쪽 시프트, 오른쪽 시프트 | `Int` 또는 `BigInt`
 `<`, `<=`, `>`, `>=` | 이진 | 보다 작음, 작거나 같음, 보다 큼, 보다 큼, 크거나 같음 비교 | `Int`, `BigInt` 또는`Double`
 `==`, `!=` | 이진 | 같음, 같지 않음 비교 | 모든 기본 형식
 `&&&` | 이진 | 비트 AND | `Int` 또는 `BigInt`
 `^^^` | 이진 | 비트 XOR | `Int` 또는 `BigInt`
 <code>\|\|\|</code> | 이진 | 비트 OR | `Int` 또는 `BigInt`
 `and` | 이진 | 논리적 AND | `Bool`
 `or` | 이진 | 논리적 OR | `Bool`
 `..` | Binary/삼항 | Range 연산자 | `Int`
 `?` `|` | 진 | 조건부 | `Bool`왼쪽의 경우
`w/` `<-` | 진 | 복사 및 업데이트 | [복사 및 업데이트 식](#copy-and-update-expressions) 참조

## <a name="next-steps"></a>다음 단계

이제 Q #에서 식 작업을 수행할 수 있으므로 [q #의 작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions) 를 사용 하 여 작업 및 함수를 정의 하 고 호출 하는 방법을 배울 수 있습니다.
