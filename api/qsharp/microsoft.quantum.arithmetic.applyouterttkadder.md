---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterTTKAdder
title: ApplyOuterTTKAdder 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterTTKAdder
qsharp.summary: Implements the outer operation for RippleCarryAdderTTK to conjugate the inner operation to construct the full adder.
ms.openlocfilehash: afcc3085965907b7478b513028e25d1813cf7b76
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843695"
---
# <a name="applyouterttkadder-operation"></a><span data-ttu-id="25238-102">ApplyOuterTTKAdder 작업</span><span class="sxs-lookup"><span data-stu-id="25238-102">ApplyOuterTTKAdder operation</span></span>

<span data-ttu-id="25238-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="25238-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="25238-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="25238-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="25238-105">RippleCarryAdderTTK에 대 한 외부 작업을 구현 하 여 전체 adder를 생성 하는 내부 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="25238-105">Implements the outer operation for RippleCarryAdderTTK to conjugate the inner operation to construct the full adder.</span></span>

```qsharp
operation ApplyOuterTTKAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="25238-106">입력</span><span class="sxs-lookup"><span data-stu-id="25238-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="25238-107">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="25238-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="25238-108">LittleEndian cobit summand 입력을 RippleCarryAdderTTK에 첫 번째 정수를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="25238-108">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="25238-109">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="25238-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="25238-110">LittleEndian cobit는 두 번째 정수 summand 입력을 RippleCarryAdderTTK에 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="25238-110">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderTTK.</span></span>



## <a name="output--unit"></a><span data-ttu-id="25238-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="25238-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="25238-112">참조</span><span class="sxs-lookup"><span data-stu-id="25238-112">References</span></span>

- <span data-ttu-id="25238-113">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "퀀텀 추가 회로 및 무제한 팬 아웃", 퀀텀 정보 및 계산, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="25238-113">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530