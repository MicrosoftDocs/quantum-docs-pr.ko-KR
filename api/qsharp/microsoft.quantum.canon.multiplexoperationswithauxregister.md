---
uid: Microsoft.Quantum.Canon.MultiplexOperationsWithAuxRegister
title: MultiplexOperationsWithAuxRegister 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsWithAuxRegister
qsharp.summary: Implementation step of MultiplexOperations.
ms.openlocfilehash: f6a90657324f8528aaa2e9e511a7f8cbcd2f540f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715793"
---
# <a name="multiplexoperationswithauxregister-operation"></a><span data-ttu-id="f022a-102">MultiplexOperationsWithAuxRegister 작업</span><span class="sxs-lookup"><span data-stu-id="f022a-102">MultiplexOperationsWithAuxRegister operation</span></span>

<span data-ttu-id="f022a-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f022a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f022a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f022a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f022a-105">MultiplexOperations의 구현 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="f022a-105">Implementation step of MultiplexOperations.</span></span>

```qsharp
operation MultiplexOperationsWithAuxRegister<'T> (unitaries : ('T => Unit is Adj + Ctl)[], auxillaryRegister : Qubit[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="f022a-106">입력</span><span class="sxs-lookup"><span data-stu-id="f022a-106">Input</span></span>

### <a name="unitaries--t--unit-adj--ctl"></a><span data-ttu-id="f022a-107">unitaries: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl []</span><span class="sxs-lookup"><span data-stu-id="f022a-107">unitaries : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl[]</span></span>




### <a name="auxillaryregister--qubit"></a><span data-ttu-id="f022a-108">auxillaryRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f022a-108">auxillaryRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="index--littleendian"></a><span data-ttu-id="f022a-109">인덱스: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f022a-109">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>




### <a name="target--t"></a><span data-ttu-id="f022a-110">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="f022a-110">target : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="f022a-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f022a-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f022a-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f022a-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f022a-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="f022a-113">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="f022a-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f022a-114">See Also</span></span>

- [<span data-ttu-id="f022a-115">MultiplexOperations입니다.</span><span class="sxs-lookup"><span data-stu-id="f022a-115">Microsoft.Quantum.Canon.MultiplexOperations</span></span>](xref:Microsoft.Quantum.Canon.MultiplexOperations)