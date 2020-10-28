---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: ArrangedQubits 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 7f5cce3429b72f0ff6e00c2079241272881512da
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716745"
---
# <a name="arrangedqubits-function"></a>ArrangedQubits 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


인덱스에 따라 컨트롤, 대상 및 도우미의 정렬

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a>Description

인덱스 0에서 target을 사용 하 고 인덱스 2 ^ i에서 컨트롤 i를 사용 하 여 원하는 비트 배열을 반환 합니다.  도우미는 배열의 다른 모든 위치에 삽입 됩니다.

## <a name="input"></a>입력

### <a name="controls--qubit"></a>컨트롤: [이상](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="target--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)




### <a name="helper--qubit"></a>도우미:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[]





## <a name="output--qubit"></a>출력: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

