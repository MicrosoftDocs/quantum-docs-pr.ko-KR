---
uid: Microsoft.Quantum.Simulation.BlockEncodingToReflection
title: BlockEncodingToReflection 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingToReflection
qsharp.summary: >-
  Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.

  That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$. This increases the size of the auxiliary register of $U$ by one qubit.
ms.openlocfilehash: bada0dcc54d2a8d67cf7383d7153c7f46a4a8415
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847270"
---
# <a name="blockencodingtoreflection-function"></a>BlockEncodingToReflection 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


을 해당 하는으로 변환 합니다 `BlockEncoding` `BLockEncodingReflection` .

즉, 특정 `BlockEncoding` $H 연산자 ($)를 인코딩하는 단일 $U $가 지정 된 경우,이 연산자를 `BlockEncodingReflection` 동일한 연산자를 인코딩하는 $U ' $로 변환 하 고, $U ' ^ \A턴 = U ' $를 충족 합니다.
그러면 $U $의 보조 레지스터 크기가 1 배 비트로 늘어납니다.

```qsharp
function BlockEncodingToReflection (blockEncoding : Microsoft.Quantum.Simulation.BlockEncoding) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a>입력

### <a name="blockencoding--blockencoding"></a>blockEncoding: [Blockencoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)

`BlockEncoding`리플렉션으로 변환할 단일 $U $입니다.



## <a name="output--blockencodingreflection"></a>출력: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)

단일 $U ' $는 레지스터에 대해 공동으로 작동 `a` 하며 `s` $H $를 차단 하 고 $U ' ^ \A턴 = U ' $를 충족 합니다.

## <a name="remarks"></a>설명

그러면 $U $의 보조 레지스터 크기가 1 배 비트로 늘어납니다.

## <a name="references"></a>참조

- Hamiltonian 시뮬레이션의 Guang Jia-hao Low, Isaac Chuang https://arxiv.org/abs/1610.06546

## <a name="see-also"></a>참고 항목

- [Microsoft 양자. 블록 인코딩](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [BlockEncodingReflection.](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)