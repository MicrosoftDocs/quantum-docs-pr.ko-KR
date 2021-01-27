---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: IsNotZero 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: 9384e5dafd4b5b7d44cb348c9537ebc2c621466d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839594"
---
# <a name="isnotzero-function"></a>IsNotZero 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Chemistry)

패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


`Double`숫자가 약 0이 아닌지 여부를 확인 합니다.

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a>입력

### <a name="number--double"></a>숫자: [Double](xref:microsoft.quantum.lang-ref.double)

확인할 수



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`number`에 보다 큰 절대값 값이 있으면 true를 반환 `1e-15` 합니다.