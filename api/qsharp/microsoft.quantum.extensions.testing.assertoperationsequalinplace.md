---
uid: Microsoft.Quantum.Extensions.Testing.AssertOperationsEqualInPlace
title: AssertOperationsEqualInPlace 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Extensions.Testing
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  > [!WARNING]

  > AssertOperationsEqualInPlace has been deprecated. Please use <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace> instead.

  >

  > Please use @"microsoft.quantum.diagnostics.assertoperationsequalinplace".

  > Note that the order of the arguments to this operation has changed.
ms.openlocfilehash: 6d2ead95a60ed3cc8ee95fb7f91e1aa49d366a48
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711677"
---
# <a name="assertoperationsequalinplace-operation"></a><span data-ttu-id="1d05a-102">AssertOperationsEqualInPlace 작업</span><span class="sxs-lookup"><span data-stu-id="1d05a-102">AssertOperationsEqualInPlace operation</span></span>

<span data-ttu-id="1d05a-103">네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Extensions.Testing) .</span><span class="sxs-lookup"><span data-stu-id="1d05a-103">Namespace: [Microsoft.Quantum.Extensions.Testing](xref:Microsoft.Quantum.Extensions.Testing)</span></span>

<span data-ttu-id="1d05a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1d05a-104">Package: [](https://nuget.org/packages/)</span></span>


> [!WARNING]
> <span data-ttu-id="1d05a-105">AssertOperationsEqualInPlace는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d05a-105">AssertOperationsEqualInPlace has been deprecated.</span></span> <span data-ttu-id="1d05a-106">대신 <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace>를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="1d05a-106">Please use <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace> instead.</span></span>
>
> <span data-ttu-id="1d05a-107">@"microsoft.quantum.diagnostics.assertoperationsequalinplace"을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="1d05a-107">Please use @"microsoft.quantum.diagnostics.assertoperationsequalinplace".</span></span>
> <span data-ttu-id="1d05a-108">이 작업에 대 한 인수의 순서가 변경 된 것을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d05a-108">Note that the order of the arguments to this operation has changed.</span></span>



```qsharp
operation AssertOperationsEqualInPlace (actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj), nQubits : Int) : Unit
```


## <a name="input"></a><span data-ttu-id="1d05a-109">입력</span><span class="sxs-lookup"><span data-stu-id="1d05a-109">Input</span></span>

### <a name="actual--qubit--unit"></a><span data-ttu-id="1d05a-110">actual: [bit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1d05a-110">actual : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="expected--qubit--unit-adj"></a><span data-ttu-id="1d05a-111">예상: 이상 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="1d05a-111">expected : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>




### <a name="nqubits--int"></a><span data-ttu-id="1d05a-112">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1d05a-112">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--unit"></a><span data-ttu-id="1d05a-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1d05a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

