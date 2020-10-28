---
uid: Microsoft.Quantum.ErrorCorrection.ApplyBitFlipEncoder
title: ApplyBitFlipEncoder 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: ApplyBitFlipEncoder
qsharp.summary: >-
  Private operation used to implement both the bit flip encoder and decoder.

  Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`. In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.
ms.openlocfilehash: 4d78cbb5892aabc600321185641bbf217bd4d745
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712517"
---
# <a name="applybitflipencoder-operation"></a><span data-ttu-id="0b02c-102">ApplyBitFlipEncoder 작업</span><span class="sxs-lookup"><span data-stu-id="0b02c-102">ApplyBitFlipEncoder operation</span></span>

<span data-ttu-id="0b02c-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="0b02c-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="0b02c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0b02c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0b02c-105">비트 플립 인코더와 디코더를 모두 구현 하는 데 사용 되는 개인 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0b02c-105">Private operation used to implement both the bit flip encoder and decoder.</span></span>

<span data-ttu-id="0b02c-106">이 인코더는 현재 위치의 일관 된 복구를 사용할 수 있으며,이 경우의 초기 상태에 설명 된 오류를 "발생" 시킵니다 `auxQubits` .</span><span class="sxs-lookup"><span data-stu-id="0b02c-106">Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`.</span></span>
<span data-ttu-id="0b02c-107">특히 `auxQubits` 이 $ \ket $ 상태에 있는 경우에는 {10} 인코딩된 비트의 $X _1 $ 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b02c-107">In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.</span></span>

```qsharp
operation ApplyBitFlipEncoder (coherentRecovery : Bool, data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="0b02c-108">입력</span><span class="sxs-lookup"><span data-stu-id="0b02c-108">Input</span></span>

### <a name="coherentrecovery--bool"></a><span data-ttu-id="0b02c-109">coherentRecovery: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="0b02c-109">coherentRecovery : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="data--qubit"></a><span data-ttu-id="0b02c-110">data: [bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="0b02c-110">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="scratch--qubit"></a><span data-ttu-id="0b02c-111">스크래치: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="0b02c-111">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="0b02c-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0b02c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="0b02c-113">참조</span><span class="sxs-lookup"><span data-stu-id="0b02c-113">References</span></span>

- <span data-ttu-id="0b02c-114">doi: 10.1103/PhysRevA 85.044302</span><span class="sxs-lookup"><span data-stu-id="0b02c-114">doi:10.1103/PhysRevA.85.044302</span></span>