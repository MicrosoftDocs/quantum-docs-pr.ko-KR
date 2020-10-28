---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: SteaneCodeEncoderImpl 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: b843422a6007d01de9b57ec659c229b8ab0ad2e6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712188"
---
# <a name="steanecodeencoderimpl-operation"></a><span data-ttu-id="51279-102">SteaneCodeEncoderImpl 작업</span><span class="sxs-lookup"><span data-stu-id="51279-102">SteaneCodeEncoderImpl operation</span></span>

<span data-ttu-id="51279-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="51279-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="51279-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="51279-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="51279-105">Steane 코드 인코더와 디코더를 모두 구현 하는 데 사용 되는 개인 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="51279-105">Private operation used to implement both the Steane code encoder and decoder.</span></span>

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="51279-106">입력</span><span class="sxs-lookup"><span data-stu-id="51279-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="51279-107">data: [bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="51279-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="51279-108">입력의 비트를 포함 하는 1 개의 비트를 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="51279-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="51279-109">스크래치: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="51279-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="51279-110">중복성을 추가 하는 6 개의 비트를 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="51279-110">an array holding 6 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="51279-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="51279-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

