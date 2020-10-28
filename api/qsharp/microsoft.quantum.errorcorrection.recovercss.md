---
uid: Microsoft.Quantum.ErrorCorrection.RecoverCSS
title: RecoverCSS 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoverCSS
qsharp.summary: Performs a single round of error correction by a quantum code described by a `CSS` type.
ms.openlocfilehash: 48d3cd3d5f6aea265fac2f50b913ab855a31accf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712202"
---
# <a name="recovercss-operation"></a><span data-ttu-id="40a07-102">RecoverCSS 작업</span><span class="sxs-lookup"><span data-stu-id="40a07-102">RecoverCSS operation</span></span>

<span data-ttu-id="40a07-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="40a07-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="40a07-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="40a07-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="40a07-105">형식으로 설명 되는 퀀텀 코드에의 한 오류 수정 사항을 한 번 수행 합니다 `CSS` .</span><span class="sxs-lookup"><span data-stu-id="40a07-105">Performs a single round of error correction by a quantum code described by a `CSS` type.</span></span>

```qsharp
operation RecoverCSS (code : Microsoft.Quantum.ErrorCorrection.CSS, fnX : Microsoft.Quantum.ErrorCorrection.RecoveryFn, fnZ : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a><span data-ttu-id="40a07-106">입력</span><span class="sxs-lookup"><span data-stu-id="40a07-106">Input</span></span>

### <a name="code--css"></a><span data-ttu-id="40a07-107">코드: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="40a07-107">code : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="40a07-108">퀀텀 CSS 오류-형식으로 패키지 된 코드를 수정 하면 `CSS` 퀀텀 데이터의 인코딩과 디코딩을 설명 하 고 오류 syndromes을 측정 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="40a07-108">A quantum CSS error-correcting code packaged as a `CSS` type describes the encoding and decoding of quantum data, and how error syndromes are to be measured.</span></span>


### <a name="fnx--recoveryfn"></a><span data-ttu-id="40a07-109">fnX: [Recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="40a07-109">fnX : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="40a07-110">`RecoveryFn`검색 된 오류를 수정 하는 작업에 각 $X $ error 증후군를 매핑하는입니다 `Pauli[]` .</span><span class="sxs-lookup"><span data-stu-id="40a07-110">A `RecoveryFn` that maps each $X$ error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="fnz--recoveryfn"></a><span data-ttu-id="40a07-111">fnZ: [Recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="40a07-111">fnZ : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="40a07-112">`RecoveryFn`검색 된 오류를 수정 하는 작업에 각 $Z $ error 증후군를 매핑하는입니다 `Pauli[]` .</span><span class="sxs-lookup"><span data-stu-id="40a07-112">A `RecoveryFn` that maps each $Z$ error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="40a07-113">logicalRegister: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="40a07-113">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="40a07-114">안정기 코드가 정의 된 요소의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="40a07-114">An array of qubits where the stabilizer code is defined.</span></span>



## <a name="output--unit"></a><span data-ttu-id="40a07-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="40a07-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="40a07-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="40a07-116">See Also</span></span>

- [<span data-ttu-id="40a07-117">Microsoft. Errorerror.css</span><span class="sxs-lookup"><span data-stu-id="40a07-117">Microsoft.Quantum.ErrorCorrection.CSS</span></span>](xref:Microsoft.Quantum.ErrorCorrection.CSS)
- [<span data-ttu-id="40a07-118">Microsoft 양자를 수정 합니다. RecoveryFn</span><span class="sxs-lookup"><span data-stu-id="40a07-118">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [<span data-ttu-id="40a07-119">Microsoft 양자를 수정 합니다. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="40a07-119">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)