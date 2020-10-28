---
uid: Microsoft.Quantum.Canon.RAll1
title: RAll1 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RAll1
qsharp.summary: >-
  Performs a phase shift operation.

  $R=\boldone-(1-e^{i \phi})\ket{1\cdots 1}\bra{1\cdots 1}$.
ms.openlocfilehash: 45892f9811faf56d7b9a0eb34e4bde0a32d5586d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715625"
---
# <a name="rall1-operation"></a><span data-ttu-id="c963a-102">RAll1 작업</span><span class="sxs-lookup"><span data-stu-id="c963a-102">RAll1 operation</span></span>

<span data-ttu-id="c963a-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c963a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c963a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c963a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c963a-105">단계 이동 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c963a-105">Performs a phase shift operation.</span></span>

<span data-ttu-id="c963a-106">$R = \boldone-(1-e ^ {i \phi}) \ket{1\cdots 1} \bra{1\cdots 1} $.</span><span class="sxs-lookup"><span data-stu-id="c963a-106">$R=\boldone-(1-e^{i \phi})\ket{1\cdots 1}\bra{1\cdots 1}$.</span></span>

```qsharp
operation RAll1 (phase : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="c963a-107">입력</span><span class="sxs-lookup"><span data-stu-id="c963a-107">Input</span></span>

### <a name="phase--double"></a><span data-ttu-id="c963a-108">단계: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c963a-108">phase : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c963a-109">$ \\\A$ 단계는 $ \ket{1\cdots 1} \bra{1\cdots 1} $ 상태에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c963a-109">The phase $\phi$ applied to state $\ket{1\cdots 1}\bra{1\cdots 1}$.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="c963a-110">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c963a-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c963a-111">$R $에서 해당 상태를 회전할 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="c963a-111">The register whose state is to be rotated by $R$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c963a-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c963a-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

