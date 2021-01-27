---
uid: Microsoft.Quantum.Diagnostics._assertEqualOnBasisVector
title: _assertEqualOnBasisVector 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _assertEqualOnBasisVector
qsharp.summary: Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same. The basis state is described by `basis` parameter. See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.
ms.openlocfilehash: 041fecfa27ae5bd17fa8fdc89ce964f985f6124b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853593"
---
# <a name="_assertequalonbasisvector-operation"></a><span data-ttu-id="cc8fc-102">_assertEqualOnBasisVector 작업</span><span class="sxs-lookup"><span data-stu-id="cc8fc-102">_assertEqualOnBasisVector operation</span></span>

<span data-ttu-id="cc8fc-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="cc8fc-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="cc8fc-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="cc8fc-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="cc8fc-105">두 작업과 `givenU` 기반 상태를 적용 한 결과가 동일한 지 확인 합니다 `expectedU` .</span><span class="sxs-lookup"><span data-stu-id="cc8fc-105">Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same.</span></span> <span data-ttu-id="cc8fc-106">기본 상태는 매개 변수를 통해 설명 됩니다 `basis` .</span><span class="sxs-lookup"><span data-stu-id="cc8fc-106">The basis state is described by `basis` parameter.</span></span>
<span data-ttu-id="cc8fc-107"><xref:microsoft.quantum.extensions.fliptobasis>이 설명에 대 한 자세한 내용은 함수를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cc8fc-107">See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.</span></span>

```qsharp
operation _assertEqualOnBasisVector (basis : Int[], givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="cc8fc-108">입력</span><span class="sxs-lookup"><span data-stu-id="cc8fc-108">Input</span></span>

### <a name="basis--int"></a><span data-ttu-id="cc8fc-109">기본: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="cc8fc-109">basis : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="cc8fc-110">각 $n $ 이상 비트에 대해 단일가 지정 하는 기준 상태 (0 <= id <= 3)입니다.</span><span class="sxs-lookup"><span data-stu-id="cc8fc-110">Basis state specified by a single-qubit basis state ID (0 <= id <= 3) for each of $n$ qubits.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="cc8fc-111">givenU: [](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cc8fc-111">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="cc8fc-112">검사 될 $ 이상 비트 $n에 대 한 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="cc8fc-112">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit--is-adj"></a><span data-ttu-id="cc8fc-113">Adj [= []](xref:microsoft.quantum.lang-ref.qubit)=> [Unit](xref:microsoft.quantum.lang-ref.unit)  이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc8fc-113">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="cc8fc-114">GivenU $n에 대 한 참조 작업을 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc8fc-114">Reference operation on $n$ qubits that givenU is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cc8fc-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cc8fc-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

