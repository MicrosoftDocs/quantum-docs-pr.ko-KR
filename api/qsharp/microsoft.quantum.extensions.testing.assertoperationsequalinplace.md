---
uid: Microsoft.Quantum.Extensions.Testing.AssertOperationsEqualInPlace
title: AssertOperationsEqualInPlace 작업
ms.date: 11/25/2020 12:00:00 AM
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
ms.openlocfilehash: 0f22bcbf74a33b1501acf9222d6dc6327b16bbbe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212548"
---
# <a name="assertoperationsequalinplace-operation"></a><span data-ttu-id="459ec-102">AssertOperationsEqualInPlace 작업</span><span class="sxs-lookup"><span data-stu-id="459ec-102">AssertOperationsEqualInPlace operation</span></span>

<span data-ttu-id="459ec-103">네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Extensions.Testing) .</span><span class="sxs-lookup"><span data-stu-id="459ec-103">Namespace: [Microsoft.Quantum.Extensions.Testing](xref:Microsoft.Quantum.Extensions.Testing)</span></span>

<span data-ttu-id="459ec-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="459ec-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


> [!WARNING]
> <span data-ttu-id="459ec-105">AssertOperationsEqualInPlace는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="459ec-105">AssertOperationsEqualInPlace has been deprecated.</span></span> <span data-ttu-id="459ec-106">대신 <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace>를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="459ec-106">Please use <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace> instead.</span></span>
>
> <span data-ttu-id="459ec-107">@"microsoft.quantum.diagnostics.assertoperationsequalinplace"을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="459ec-107">Please use @"microsoft.quantum.diagnostics.assertoperationsequalinplace".</span></span>
> <span data-ttu-id="459ec-108">이 작업에 대 한 인수의 순서가 변경 된 것을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="459ec-108">Note that the order of the arguments to this operation has changed.</span></span>



```qsharp
operation AssertOperationsEqualInPlace (actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj), nQubits : Int) : Unit
```


## <a name="input"></a><span data-ttu-id="459ec-109">입력</span><span class="sxs-lookup"><span data-stu-id="459ec-109">Input</span></span>

### <a name="actual--qubit--unit"></a><span data-ttu-id="459ec-110">actual: [bit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="459ec-110">actual : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="expected--qubit--unit--is-adj"></a><span data-ttu-id="459ec-111">예상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="459ec-111">expected : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="nqubits--int"></a><span data-ttu-id="459ec-112">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="459ec-112">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--unit"></a><span data-ttu-id="459ec-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="459ec-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

