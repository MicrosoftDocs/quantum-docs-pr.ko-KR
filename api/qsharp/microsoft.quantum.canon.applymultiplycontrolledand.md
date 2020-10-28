---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledAnd
title: ApplyMultiplyControlledAnd 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.
ms.openlocfilehash: feca28d394e4af31eb4ffe737111d00ede45e27e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717956"
---
# <a name="applymultiplycontrolledand-operation"></a><span data-ttu-id="c1686-102">ApplyMultiplyControlledAnd 작업</span><span class="sxs-lookup"><span data-stu-id="c1686-102">ApplyMultiplyControlledAnd operation</span></span>

<span data-ttu-id="c1686-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c1686-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c1686-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c1686-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c1686-105">는 해당 대상의 비트를 0으로 초기화 한다고 가정 하 고 다중 제어 된 Toffoli gate를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1686-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="c1686-106">Adjoint 연산은 대상의 비트를 0으로 다시 설정 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1686-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>

```qsharp
operation ApplyMultiplyControlledAnd (controls : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="c1686-107">입력</span><span class="sxs-lookup"><span data-stu-id="c1686-107">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="c1686-108">컨트롤: [이상](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c1686-108">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c1686-109">제어 비트</span><span class="sxs-lookup"><span data-stu-id="c1686-109">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="c1686-110">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c1686-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c1686-111">대상 비트</span><span class="sxs-lookup"><span data-stu-id="c1686-111">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="c1686-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c1686-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

