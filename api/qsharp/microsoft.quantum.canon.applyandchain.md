---
uid: Microsoft.Quantum.Canon.ApplyAndChain
title: ApplyAndChain 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAndChain
qsharp.summary: Computes a chain of AND gates
ms.openlocfilehash: 3991ded1a9c70bf4b58d19b0304a1df3b31896d0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842011"
---
# <a name="applyandchain-operation"></a><span data-ttu-id="667bd-102">ApplyAndChain 작업</span><span class="sxs-lookup"><span data-stu-id="667bd-102">ApplyAndChain operation</span></span>

<span data-ttu-id="667bd-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="667bd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="667bd-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="667bd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="667bd-105">및 게이트 체인을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="667bd-105">Computes a chain of AND gates</span></span>

```qsharp
operation ApplyAndChain (auxRegister : Qubit[], ctrlRegister : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="667bd-106">설명</span><span class="sxs-lookup"><span data-stu-id="667bd-106">Description</span></span>

<span data-ttu-id="667bd-107">임시 결과를 계산 하는 보조 비트를 명시적으로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="667bd-107">The auxiliary qubits to compute temporary results must be specified explicitly.</span></span>
<span data-ttu-id="667bd-108">해당 레지스터의 길이는 `Length(ctrlRegister) - 2` 두 개 이상의 컨트롤이 있는 경우이 고, 그렇지 않으면 길이가 0입니다.</span><span class="sxs-lookup"><span data-stu-id="667bd-108">The length of that register is `Length(ctrlRegister) - 2`, if there are at least two controls, otherwise the length is 0.</span></span>

## <a name="input"></a><span data-ttu-id="667bd-109">입력</span><span class="sxs-lookup"><span data-stu-id="667bd-109">Input</span></span>

### <a name="auxregister--qubit"></a><span data-ttu-id="667bd-110">auxRegister: [](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="667bd-110">auxRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="ctrlregister--qubit"></a><span data-ttu-id="667bd-111">ctrlRegister: [](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="667bd-111">ctrlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="667bd-112">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="667bd-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="667bd-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="667bd-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

