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
# <a name="tablelookuprecovery-function"></a><span data-ttu-id="914c4-102">TableLookupRecovery 함수</span><span class="sxs-lookup"><span data-stu-id="914c4-102">TableLookupRecovery function</span></span>

<span data-ttu-id="914c4-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="914c4-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="914c4-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="914c4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="914c4-105">지정 된 양의 비트 레지스터에서 지정 된 Pauli 작업 테이블의 경우이 함수는 `RecoveryFn` 지정 된 Pauli 작업 배열과 관련 하 여 테이블 조회 디코딩을 수행 하는 데 필요한 모든 정보를 포함 하는 형식의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="914c4-105">For a given table of Pauli operations on a given register of qubits, this function returns an object of type `RecoveryFn` which contains all information needed to perform a table-lookup decoding with respect to the given array of Pauli operations.</span></span>

```qsharp
function TableLookupRecovery (table : Pauli[][]) : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="input"></a><span data-ttu-id="914c4-106">입력</span><span class="sxs-lookup"><span data-stu-id="914c4-106">Input</span></span>

### <a name="table--pauli"></a><span data-ttu-id="914c4-107">테이블: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="914c4-107">table : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="914c4-108">지정 된 고 비트 레지스터에서 작동 하는 Pauli 작업 표</span><span class="sxs-lookup"><span data-stu-id="914c4-108">Table of Pauli operations that operate on a given qubit register</span></span>



## <a name="output--recoveryfn"></a><span data-ttu-id="914c4-109">출력: [Recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="914c4-109">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="914c4-110">`RecoveryFn` `Syndrome -> Pauli[]` 지정 된 증후군 배열에 해당 하는 Pauli 수정 작업을 연결 하는 map 형식의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="914c4-110">An object of type `RecoveryFn`, i.e., a map `Syndrome -> Pauli[]` that associates with a given syndrome array a corresponding Pauli correction operation.</span></span>