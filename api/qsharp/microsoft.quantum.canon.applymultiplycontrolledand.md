---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledAnd
title: ApplyMultiplyControlledAnd 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.
ms.openlocfilehash: ac3972287d55ed2df85e1d88510918cc5202c711
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844850"
---
# <a name="applymultiplycontrolledand-operation"></a><span data-ttu-id="2f4d2-102">ApplyMultiplyControlledAnd 작업</span><span class="sxs-lookup"><span data-stu-id="2f4d2-102">ApplyMultiplyControlledAnd operation</span></span>

<span data-ttu-id="2f4d2-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2f4d2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2f4d2-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2f4d2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2f4d2-105">는 해당 대상의 비트를 0으로 초기화 한다고 가정 하 고 다중 제어 된 Toffoli gate를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f4d2-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="2f4d2-106">Adjoint 연산은 대상의 비트를 0으로 다시 설정 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f4d2-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>

```qsharp
operation ApplyMultiplyControlledAnd (controls : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="2f4d2-107">입력</span><span class="sxs-lookup"><span data-stu-id="2f4d2-107">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="2f4d2-108">컨트롤: [이상](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="2f4d2-108">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="2f4d2-109">제어 비트</span><span class="sxs-lookup"><span data-stu-id="2f4d2-109">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="2f4d2-110">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="2f4d2-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="2f4d2-111">대상 비트</span><span class="sxs-lookup"><span data-stu-id="2f4d2-111">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="2f4d2-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2f4d2-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

