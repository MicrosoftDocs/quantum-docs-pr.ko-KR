---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoderImpl
title: FiveQubitCodeEncoderImpl 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeEncoderImpl
qsharp.summary: Private operation used to implement both the 5 qubit encoder and decoder.
ms.openlocfilehash: 29b0f47ddffeae3ed4dfda4084304427418e02fd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712335"
---
# <a name="fivequbitcodeencoderimpl-operation"></a><span data-ttu-id="62145-102">FiveQubitCodeEncoderImpl 작업</span><span class="sxs-lookup"><span data-stu-id="62145-102">FiveQubitCodeEncoderImpl operation</span></span>

<span data-ttu-id="62145-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="62145-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="62145-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="62145-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="62145-105">5 비트 인코더와 디코더를 모두 구현 하는 데 사용 되는 개인 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="62145-105">Private operation used to implement both the 5 qubit encoder and decoder.</span></span>

```qsharp
operation FiveQubitCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="62145-106">입력</span><span class="sxs-lookup"><span data-stu-id="62145-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="62145-107">data: [bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="62145-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="62145-108">입력의 비트를 포함 하는 1 개의 비트를 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="62145-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="62145-109">스크래치: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="62145-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="62145-110">중복성을 추가 하는 4 개의 비트를 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="62145-110">an array holding 4 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="62145-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="62145-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="62145-112">설명</span><span class="sxs-lookup"><span data-stu-id="62145-112">Remarks</span></span>

<span data-ttu-id="62145-113">선택한 특정 인코더는 Kliuchnikov 및 D. Maslov, "Clifford 회로의 최적화", 88 Phys, 052307 (2013);에서 가져온 것입니다. https://arxiv.org/abs/1305.0810, 그림 4b)를 사용 하는 경우 총 11 개의 게이트가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="62145-113">The particular encoder chosen was taken from the paper V. Kliuchnikov and D. Maslov, "Optimization of Clifford Circuits," Phys. Rev. Phys. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Figure 4b) and requires a total of 11 gates.</span></span>