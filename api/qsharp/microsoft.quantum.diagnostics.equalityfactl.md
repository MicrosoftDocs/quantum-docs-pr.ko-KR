---
uid: Microsoft.Quantum.Diagnostics.EqualityFactL
title: EqualityFactL 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactL
qsharp.summary: Asserts that a classical BigInt variable has the expected value.
ms.openlocfilehash: b7d37b5115c51596c1b3ed93c53a29e9f36b811d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829137"
---
# <a name="equalityfactl-function"></a><span data-ttu-id="3e8ef-102">EqualityFactL 함수</span><span class="sxs-lookup"><span data-stu-id="3e8ef-102">EqualityFactL function</span></span>

<span data-ttu-id="3e8ef-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="3e8ef-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="3e8ef-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3e8ef-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3e8ef-105">기존 BigInt 변수에 필요한 값이 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e8ef-105">Asserts that a classical BigInt variable has the expected value.</span></span>

```qsharp
function EqualityFactL (actual : BigInt, expected : BigInt, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="3e8ef-106">입력</span><span class="sxs-lookup"><span data-stu-id="3e8ef-106">Input</span></span>

### <a name="actual--bigint"></a><span data-ttu-id="3e8ef-107">actual: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="3e8ef-107">actual : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="3e8ef-108">확인할 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="3e8ef-108">The number to be checked.</span></span>


### <a name="expected--bigint"></a><span data-ttu-id="3e8ef-109">예상: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="3e8ef-109">expected : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="3e8ef-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3e8ef-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="3e8ef-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="3e8ef-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="3e8ef-112">어설션이 트리거될 때 사용할 오류 메시지 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="3e8ef-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3e8ef-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3e8ef-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

