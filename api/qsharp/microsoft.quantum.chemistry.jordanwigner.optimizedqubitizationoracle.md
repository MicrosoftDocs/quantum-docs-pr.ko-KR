---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedQubitizationOracle
title: OptimizedQubitizationOracle 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedQubitizationOracle
qsharp.summary: Returns T-count optimized Qubitization operation and the parameters necessary to run it.
ms.openlocfilehash: c67dc5890fe1444c1689eb803ed3d24b2dbe5ce2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713889"
---
# <a name="optimizedqubitizationoracle-function"></a><span data-ttu-id="23db9-102">OptimizedQubitizationOracle 함수</span><span class="sxs-lookup"><span data-stu-id="23db9-102">OptimizedQubitizationOracle function</span></span>

<span data-ttu-id="23db9-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="23db9-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="23db9-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="23db9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="23db9-105">T-count에 최적화 된 작업 및이 작업을 실행 하는 데 필요한 매개 변수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="23db9-105">Returns T-count optimized Qubitization operation and the parameters necessary to run it.</span></span>

```qsharp
function OptimizedQubitizationOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, targetError : Double) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a><span data-ttu-id="23db9-106">입력</span><span class="sxs-lookup"><span data-stu-id="23db9-106">Input</span></span>

### <a name="qsharpdata--jordanwignerencodingdata"></a><span data-ttu-id="23db9-107">qSharpData: [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="23db9-107">qSharpData : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="23db9-108">Hamiltonian은 형식으로 설명 `JordanWignerEncodingData` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="23db9-108">Hamiltonian described by `JordanWignerEncodingData` format.</span></span>


### <a name="targeterror--double"></a><span data-ttu-id="23db9-109">targetError: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="23db9-109">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="23db9-110">보조 상태 준비 단계 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="23db9-110">Error of auxillary state preparation step.</span></span>



## <a name="output--intdoublequbit--unit-adj--ctl"></a><span data-ttu-id="23db9-111">Output: ([Int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[intbit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl))</span><span class="sxs-lookup"><span data-stu-id="23db9-111">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl))</span></span>

<span data-ttu-id="23db9-112">튜플 (: `Int` )은 할당 된 값이 고,는 Hamiltonian 계수는 하나 이며, 작업은이 작업은이를 `Double` 통해 생성 된 퀀텀 탐색입니다.</span><span class="sxs-lookup"><span data-stu-id="23db9-112">A tuple where: `Int` is the number of qubits allocated, `Double` is the one-norm of Hamiltonian coefficients, and the operation is the Quantum walk created by Qubitization.</span></span>