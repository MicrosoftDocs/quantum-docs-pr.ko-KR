---
uid: Microsoft.Quantum.Extensions.Testing.AssertOperationsEqualReferenced
title: AssertOperationsEqualReferenced 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Extensions.Testing
qsharp.name: AssertOperationsEqualReferenced
qsharp.summary: >-
  > [!WARNING]

  > AssertOperationsEqualReferenced has been deprecated. Please use <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced> instead.

  >

  > Please use @"microsoft.quantum.diagnostics.assertoperationsequalreferenced".

  > Note that the order of the arguments to this operation has changed.
ms.openlocfilehash: 2d39f74c68e48d2f2b8003b76885c9444056f8d2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711621"
---
# <a name="assertoperationsequalreferenced-operation"></a><span data-ttu-id="09a6c-102">AssertOperationsEqualReferenced 작업</span><span class="sxs-lookup"><span data-stu-id="09a6c-102">AssertOperationsEqualReferenced operation</span></span>

<span data-ttu-id="09a6c-103">네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Extensions.Testing) .</span><span class="sxs-lookup"><span data-stu-id="09a6c-103">Namespace: [Microsoft.Quantum.Extensions.Testing](xref:Microsoft.Quantum.Extensions.Testing)</span></span>

<span data-ttu-id="09a6c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="09a6c-104">Package: [](https://nuget.org/packages/)</span></span>


> [!WARNING]
> <span data-ttu-id="09a6c-105">AssertOperationsEqualReferenced는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09a6c-105">AssertOperationsEqualReferenced has been deprecated.</span></span> <span data-ttu-id="09a6c-106">대신 <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced>를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="09a6c-106">Please use <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced> instead.</span></span>
>
> <span data-ttu-id="09a6c-107">@"microsoft.quantum.diagnostics.assertoperationsequalreferenced"을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="09a6c-107">Please use @"microsoft.quantum.diagnostics.assertoperationsequalreferenced".</span></span>
> <span data-ttu-id="09a6c-108">이 작업에 대 한 인수의 순서가 변경 된 것을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="09a6c-108">Note that the order of the arguments to this operation has changed.</span></span>



```qsharp
operation AssertOperationsEqualReferenced (actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj), nQubits : Int) : Unit
```


## <a name="input"></a><span data-ttu-id="09a6c-109">입력</span><span class="sxs-lookup"><span data-stu-id="09a6c-109">Input</span></span>

### <a name="actual--qubit--unit"></a><span data-ttu-id="09a6c-110">actual: [bit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="09a6c-110">actual : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="expected--qubit--unit-adj"></a><span data-ttu-id="09a6c-111">예상: 이상 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="09a6c-111">expected : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>




### <a name="nqubits--int"></a><span data-ttu-id="09a6c-112">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="09a6c-112">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--unit"></a><span data-ttu-id="09a6c-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="09a6c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

