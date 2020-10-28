---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: IsNotZero 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: 3c0f9c6695e8c9ec4a0953d5217c28c512ac7de1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714827"
---
# <a name="isnotzero-function"></a>IsNotZero 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Chemistry)

패키지 [](https://nuget.org/packages/)


`Double`숫자가 약 0이 아닌지 여부를 확인 합니다.

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a>입력

### <a name="number--double"></a>숫자: [Double](xref:microsoft.quantum.lang-ref.double)

확인할 수



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`number`에 보다 큰 절대값 값이 있으면 true를 반환 `1e-15` 합니다.