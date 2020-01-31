---
title: '지역 변수-Q # 기술 | Microsoft Docs'
description: '지역 변수-Q # 기술'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.local-variables
ms.openlocfilehash: 8b1de5c096210fb36a81c127a8bbbe1b39522741
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820184"
---
# <a name="local-variables"></a>지역 변수 #

`let` 키워드를 사용 하 여 작업 또는 함수 내에서 다시 사용 하기 위해 Q #의 모든 형식 값을 변수에 할당할 수 있습니다.
예를 들면 다음과 같습니다.

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

이렇게 하면 `measurementOperator`라는 변수에 Pauli 연산자의 특정 배열이 할당 됩니다.

> [!TIP]
> `let` 문의 오른쪽에 있는 식이 명확 하 고 형식이 컴파일러에 의해 유추 되기 때문에 새 변수의 형식을 명시적으로 지정할 필요가 없습니다. 

Q #의 변수는 *변경할*수 없습니다. 즉, 변수를 이러한 방식으로 정의한 후에는 어떤 방식으로든 더 이상 변경할 수 없습니다.
이렇게 하면 작업의 `Adjoint` 변형을 적용 하기 위해 다시 정렬할 변수에 적용 되는 기존 논리의 최적화를 비롯 하 여 여러 가지 유용한 최적화를 수행할 수 있습니다.

위와 같이 `let` 바인딩을 사용 하 여 정의 된 변수는 작업의 본문이 나 `for` 루프의 내용과 같은 특정 범위에 대해 로컬입니다.


## <a name="mutability"></a>가변성 ##

`let`를 사용 하 여 변수를 만드는 대신 `mutable` 키워드는 `set` 키워드를 사용 하 여 처음 생성 된 후에 다시 바인딩할 수 있는 특수 한 변경 가능한 변수를 만듭니다.

```qsharp
operation RandomInts(maxInt : Int, nrSamples : Int) : Int[] {
    mutable samples = new Int[0];
    for (i in 1 .. nrSamples) {
        set samples += [RandomInt(maxInt)];
    }
    return samples;
}
```

Q #에서 배열을 비롯 한 모든 형식은 값 의미 체계를 따릅니다. 특히 배열 항목을 업데이트할 수 없습니다. 기존 배열을 수정 하려면의 F#레코드에 대 한 것과 매우 유사한 복사 및 업데이트 메커니즘을 활용 해야 합니다. [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays)에서 제공 하는 배열에 대해 라이브러리 도구를 사용 하 여, 예를 들어, paulis의 배열을 반환 하는 함수를 쉽게 정의할 수 있습니다. 여기서는 인덱스 `i`의 Paulis가 지정 된 값을 사용 하 고 다른 모든 항목은 id입니다. 

```qsharp
function EmbedPauli (pauli : Pauli, i : Int, n : Int) : Pauli[] {
    
    let arr = ConstantArray(n, PauliI); // creates an array of filled with PauliI
    return arr w/ i <- pauli; // constructs a new array based on arr except that entry i is set to pauli
}
```

Q # 문과 식을 설명할 때 배열을 사용 하는 방법에 대해 자세히 설명 합니다. 

Q # 내의 가변성는 형식 또는 값이 아닌 *기호* 에 적용 되는 개념입니다. 구체적으로는 형식 시스템에 암시적 또는 명시적으로 표시 되지 않고 바인딩을 변경할 수 있는지 (`mutable` 키워드에 의해 표시 된 대로) 또는 변경 불가능 (`let`에 의해 표시 됨)에 대 한 변경 내용이 없습니다. 이는 특수화 된 함수 및 작업 내에서 가변성를 격리 하는 중요 한 방법을 제공 합니다.
특히 변경 가능한 변수를 사용 하는 작업에 대 한 adjoint 특수화가 자동 생성 될 수 없는 경우에도 자동 생성은 가변성를 사용 하는 함수를 호출 하는 작업에 대해 제대로 작동 합니다.
이러한 이유로 가변성를 사용 하는 함수 및 작업을 가능한 한 간단 하 고 간결한 방식으로 설정 하는 것이 좋습니다. 이렇게 하면 변경 불가능 한 일반 변수를 사용 하 여 나머지 퀀텀 프로그램을 쓸 수 있습니다.


## <a name="deconstruction"></a>분해 ##

단일 변수를 할당 하는 것 외에도 `let` 및 `mutable` 키워드를 사용 하거나, 다른 바인딩 구문을 사용 하 여 [튜플 형식의](xref:microsoft.quantum.language.type-model#tuple-types)콘텐츠를 압축 풀기도 허용 합니다.
이 폼의 할당은 해당 튜플의 요소를 *분해할* 하는 것으로 간주 됩니다.
예를 들어 튜플에 의해 Hamiltonian에서 용어를 모델링 하는 경우 분해를 사용 하 여 해당 용어로 시뮬레이트하는 데 필요한 다양 한 데이터에 액세스할 수 있습니다.

```qsharp
// Represents H = 3.1 X_0 Z_1.
let (_, (paulis, idxQubits)) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // paulis and idxQubits are both immutable variables
mutable ((c1, c2), _) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // c1 and c2 are both mutable variables
```


