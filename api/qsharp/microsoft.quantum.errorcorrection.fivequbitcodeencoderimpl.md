---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoderImpl
title: FiveQubitCodeEncoderImpl 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeEncoderImpl
qsharp.summary: Private operation used to implement both the 5 qubit encoder and decoder.
ms.openlocfilehash: 0a40d9674c011567b2fa9c838f31a0ee115e4268
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826075"
---
# <a name="fivequbitcodeencoderimpl-operation"></a><span data-ttu-id="a822c-102">FiveQubitCodeEncoderImpl 작업</span><span class="sxs-lookup"><span data-stu-id="a822c-102">FiveQubitCodeEncoderImpl operation</span></span>

<span data-ttu-id="a822c-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="a822c-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="a822c-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a822c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a822c-105">5 비트 인코더와 디코더를 모두 구현 하는 데 사용 되는 개인 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a822c-105">Private operation used to implement both the 5 qubit encoder and decoder.</span></span>

```qsharp
operation FiveQubitCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="a822c-106">입력</span><span class="sxs-lookup"><span data-stu-id="a822c-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="a822c-107">data: [bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a822c-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a822c-108">입력의 비트를 포함 하는 1 개의 비트를 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="a822c-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="a822c-109">스크래치: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a822c-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a822c-110">중복성을 추가 하는 4 개의 비트를 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="a822c-110">an array holding 4 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a822c-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a822c-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a822c-112">설명</span><span class="sxs-lookup"><span data-stu-id="a822c-112">Remarks</span></span>

<span data-ttu-id="a822c-113">선택한 특정 인코더는 Kliuchnikov 및 D. Maslov, "Clifford 회로의 최적화", 88 Phys, 052307 (2013);에서 가져온 것입니다. https://arxiv.org/abs/1305.0810, 그림 4b)를 사용 하는 경우 총 11 개의 게이트가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a822c-113">The particular encoder chosen was taken from the paper V. Kliuchnikov and D. Maslov, "Optimization of Clifford Circuits," Phys. Rev. Phys. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Figure 4b) and requires a total of 11 gates.</span></span>