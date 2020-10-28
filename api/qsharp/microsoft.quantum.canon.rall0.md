---
uid: Microsoft.Quantum.Canon.RAll0
title: RAll0 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RAll0
qsharp.summary: >-
  Performs a phase shift operation.

  $R=\boldone-(1-e^{i \phi})\ket{0\cdots 0}\bra{0\cdots 0}$.
ms.openlocfilehash: 6185e66e08d2af3aa0b35791638820b4dcc5af35
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715632"
---
# <a name="rall0-operation"></a><span data-ttu-id="51287-102">RAll0 작업</span><span class="sxs-lookup"><span data-stu-id="51287-102">RAll0 operation</span></span>

<span data-ttu-id="51287-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="51287-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="51287-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="51287-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="51287-105">단계 이동 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="51287-105">Performs a phase shift operation.</span></span>

<span data-ttu-id="51287-106">$R = \boldone-(1-e ^ {i \phi}) \ket{0\cdots 0} \bra{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="51287-106">$R=\boldone-(1-e^{i \phi})\ket{0\cdots 0}\bra{0\cdots 0}$.</span></span>

```qsharp
operation RAll0 (phase : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="51287-107">입력</span><span class="sxs-lookup"><span data-stu-id="51287-107">Input</span></span>

### <a name="phase--double"></a><span data-ttu-id="51287-108">단계: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="51287-108">phase : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="51287-109">$ \\\A$ 단계는 $ \ket{0\cdots 0} \bra{0\cdots 0} $ 상태에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51287-109">The phase $\phi$ applied to state $\ket{0\cdots 0}\bra{0\cdots 0}$.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="51287-110">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="51287-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="51287-111">$R $에서 해당 상태를 회전할 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="51287-111">The register whose state is to be rotated by $R$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="51287-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="51287-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="51287-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="51287-113">See Also</span></span>

- [<span data-ttu-id="51287-114">RAll1입니다.</span><span class="sxs-lookup"><span data-stu-id="51287-114">Microsoft.Quantum.Canon.RAll1</span></span>](xref:Microsoft.Quantum.Canon.RAll1)