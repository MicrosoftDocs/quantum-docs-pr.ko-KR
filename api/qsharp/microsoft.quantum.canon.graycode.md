---
uid: Microsoft.Quantum.Canon.GrayCode
title: GrayCode 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: fc673ae21a952788b5beb74c1bad94ee9fe54480
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716164"
---
# <a name="graycode-function"></a>GrayCode 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


회색 코드 시퀀스를 만듭니다.

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a>입력

### <a name="n--int"></a>n: [Int](xref:microsoft.quantum.lang-ref.int)

비트 수



## <a name="output--intint"></a>Output: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []

튜플 배열입니다. 튜플의 첫 번째 값은 GrayCode의 값입니다. 튜플의 값은 현재 값에서 변경 하 여 다음 항목을 가져오기 위한 위치입니다.