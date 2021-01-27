---
uid: Microsoft.Quantum.Canon.GrayCode
title: GrayCode 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: 0a9a19685f0511c44942df7d0bc8d257ad6b18c6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840492"
---
# <a name="graycode-function"></a>GrayCode 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


회색 코드 시퀀스를 만듭니다.

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a>입력

### <a name="n--int"></a>n: [Int](xref:microsoft.quantum.lang-ref.int)

비트 수



## <a name="output--intint"></a>Output: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []

튜플 배열입니다. 튜플의 첫 번째 값은 GrayCode의 값입니다. 튜플의 값은 현재 값에서 변경 하 여 다음 항목을 가져오기 위한 위치입니다.

## <a name="example"></a>예제

```qsharp
GrayCode(2); // [(0, 0),(1, 1),(3, 0),(2, 1)]
```