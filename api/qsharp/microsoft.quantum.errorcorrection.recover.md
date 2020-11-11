---
uid: Microsoft.Quantum.ErrorCorrection.Recover
title: 복구 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: Recover
qsharp.summary: Performs a single round of error correction by a quantum code described by a `QECC` type.
ms.openlocfilehash: a659399f51794a4edc1d2ff43da84e46797103fb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712209"
---
# <a name="recover-operation"></a><span data-ttu-id="801b0-102">복구 작업</span><span class="sxs-lookup"><span data-stu-id="801b0-102">Recover operation</span></span>

<span data-ttu-id="801b0-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="801b0-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="801b0-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="801b0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="801b0-105">형식으로 설명 되는 퀀텀 코드에의 한 오류 수정 사항을 한 번 수행 합니다 `QECC` .</span><span class="sxs-lookup"><span data-stu-id="801b0-105">Performs a single round of error correction by a quantum code described by a `QECC` type.</span></span>

```qsharp
operation Recover (code : Microsoft.Quantum.ErrorCorrection.QECC, fn : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a><span data-ttu-id="801b0-106">입력</span><span class="sxs-lookup"><span data-stu-id="801b0-106">Input</span></span>

### <a name="code--qecc"></a><span data-ttu-id="801b0-107">코드: [Qecc](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="801b0-107">code : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="801b0-108">퀀텀 오류-형식으로 패키지 된 코드를 수정 하면 `QECC` 퀀텀 데이터의 인코딩과 디코딩을 설명 하 고 오류 syndromes을 측정 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="801b0-108">A quantum error-correcting code packaged as a `QECC` type describes the encoding and decoding of quantum data, and how error syndromes are to be measured.</span></span>


### <a name="fn--recoveryfn"></a><span data-ttu-id="801b0-109">fn: [Recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="801b0-109">fn : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="801b0-110">`RecoveryFn`검색 된 오류를 수정 하는 작업에 증후군 각 오류를 매핑하는입니다 `Pauli[]` .</span><span class="sxs-lookup"><span data-stu-id="801b0-110">A `RecoveryFn` that maps each error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="801b0-111">logicalRegister: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="801b0-111">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="801b0-112">안정기 코드가 정의 된 요소의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="801b0-112">An array of qubits where the stabilizer code is defined.</span></span>



## <a name="output--unit"></a><span data-ttu-id="801b0-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="801b0-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="801b0-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="801b0-114">See Also</span></span>

- [<span data-ttu-id="801b0-115">Microsoft 양자 수정. QECC</span><span class="sxs-lookup"><span data-stu-id="801b0-115">Microsoft.Quantum.ErrorCorrection.QECC</span></span>](xref:Microsoft.Quantum.ErrorCorrection.QECC)
- [<span data-ttu-id="801b0-116">Microsoft 양자를 수정 합니다. RecoveryFn</span><span class="sxs-lookup"><span data-stu-id="801b0-116">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [<span data-ttu-id="801b0-117">Microsoft 양자를 수정 합니다. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="801b0-117">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)