---
uid: Microsoft.Quantum.ErrorCorrection.TableLookupRecovery
title: TableLookupRecovery 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: TableLookupRecovery
qsharp.summary: For a given table of Pauli operations on a given register of qubits, this function returns an object of type `RecoveryFn` which contains all information needed to perform a table-lookup decoding with respect to the given array of Pauli operations.
ms.openlocfilehash: 9f957155e42bb6b5163521171fcba5897f290335
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824393"
---
# <a name="tablelookuprecovery-function"></a>TableLookupRecovery 함수

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 양의 비트 레지스터에서 지정 된 Pauli 작업 테이블의 경우이 함수는 `RecoveryFn` 지정 된 Pauli 작업 배열과 관련 하 여 테이블 조회 디코딩을 수행 하는 데 필요한 모든 정보를 포함 하는 형식의 개체를 반환 합니다.

```qsharp
function TableLookupRecovery (table : Pauli[][]) : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="input"></a>입력

### <a name="table--pauli"></a>테이블: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

지정 된 고 비트 레지스터에서 작동 하는 Pauli 작업 표



## <a name="output--recoveryfn"></a>출력: [Recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

`RecoveryFn` `Syndrome -> Pauli[]` 지정 된 증후군 배열에 해당 하는 Pauli 수정 작업을 연결 하는 map 형식의 개체입니다.