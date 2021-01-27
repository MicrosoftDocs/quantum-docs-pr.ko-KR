---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: SteaneCodeEncoderImpl 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: 81abe75e2a315fe9a994147242f3c8c9bde586ed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824729"
---
# <a name="steanecodeencoderimpl-operation"></a><span data-ttu-id="fdc48-102">SteaneCodeEncoderImpl 작업</span><span class="sxs-lookup"><span data-stu-id="fdc48-102">SteaneCodeEncoderImpl operation</span></span>

<span data-ttu-id="fdc48-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="fdc48-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="fdc48-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fdc48-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fdc48-105">Steane 코드 인코더와 디코더를 모두 구현 하는 데 사용 되는 개인 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="fdc48-105">Private operation used to implement both the Steane code encoder and decoder.</span></span>

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="fdc48-106">입력</span><span class="sxs-lookup"><span data-stu-id="fdc48-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="fdc48-107">data: [bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fdc48-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="fdc48-108">입력의 비트를 포함 하는 1 개의 비트를 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="fdc48-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="fdc48-109">스크래치: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fdc48-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="fdc48-110">중복성을 추가 하는 6 개의 비트를 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="fdc48-110">an array holding 6 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fdc48-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fdc48-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

