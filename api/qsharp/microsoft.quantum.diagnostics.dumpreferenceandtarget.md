---
uid: Microsoft.Quantum.Diagnostics.DumpReferenceAndTarget
title: DumpReferenceAndTarget 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpReferenceAndTarget
qsharp.summary: Uses DumpRegister to provide diagnostics on the state of a reference and target register. Written as separate operation to allow overriding and interpreting as separate registers, rather than as a single combined register.
ms.openlocfilehash: f791f6f1e3c1b1da14ac3548a4bd78bb4f24ff83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712853"
---
# <a name="dumpreferenceandtarget-operation"></a><span data-ttu-id="81f23-102">DumpReferenceAndTarget 작업</span><span class="sxs-lookup"><span data-stu-id="81f23-102">DumpReferenceAndTarget operation</span></span>

<span data-ttu-id="81f23-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="81f23-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="81f23-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="81f23-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="81f23-105">DumpRegister를 사용 하 여 참조 및 대상 레지스터의 상태에 대 한 진단을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="81f23-105">Uses DumpRegister to provide diagnostics on the state of a reference and target register.</span></span> <span data-ttu-id="81f23-106">결합 된 단일 레지스터가 아닌 별도의 레지스터를 재정의 하 고 해석할 수 있도록 별도의 작업으로 작성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="81f23-106">Written as separate operation to allow overriding and interpreting as separate registers, rather than as a single combined register.</span></span>

```qsharp
operation DumpReferenceAndTarget (reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="81f23-107">입력</span><span class="sxs-lookup"><span data-stu-id="81f23-107">Input</span></span>

### <a name="reference--qubit"></a><span data-ttu-id="81f23-108">참조:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="81f23-108">reference : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="81f23-109">target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="81f23-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="81f23-110">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="81f23-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

