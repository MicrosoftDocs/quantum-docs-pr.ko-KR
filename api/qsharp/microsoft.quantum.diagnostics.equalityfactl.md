---
uid: Microsoft.Quantum.Diagnostics.EqualityFactL
title: EqualityFactL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactL
qsharp.summary: Asserts that a classical BigInt variable has the expected value.
ms.openlocfilehash: 5e590af581be4e41df9d2081260409c454e3be4b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712755"
---
# <a name="equalityfactl-function"></a><span data-ttu-id="88e08-102">EqualityFactL 함수</span><span class="sxs-lookup"><span data-stu-id="88e08-102">EqualityFactL function</span></span>

<span data-ttu-id="88e08-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="88e08-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="88e08-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="88e08-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="88e08-105">기존 BigInt 변수에 필요한 값이 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e08-105">Asserts that a classical BigInt variable has the expected value.</span></span>

```qsharp
function EqualityFactL (actual : BigInt, expected : BigInt, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="88e08-106">입력</span><span class="sxs-lookup"><span data-stu-id="88e08-106">Input</span></span>

### <a name="actual--bigint"></a><span data-ttu-id="88e08-107">actual: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="88e08-107">actual : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="88e08-108">확인할 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="88e08-108">The number to be checked.</span></span>


### <a name="expected--bigint"></a><span data-ttu-id="88e08-109">예상: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="88e08-109">expected : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="88e08-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="88e08-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="88e08-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="88e08-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="88e08-112">어설션이 트리거될 때 사용할 오류 메시지 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="88e08-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="88e08-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="88e08-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

