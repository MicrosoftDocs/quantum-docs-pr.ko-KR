---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: MeasureAllZ 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 4ac36a77b37f672859e61f3db89a43f4ca1fc93c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711075"
---
# <a name="measureallz-operation"></a><span data-ttu-id="2de07-102">MeasureAllZ 작업</span><span class="sxs-lookup"><span data-stu-id="2de07-102">MeasureAllZ operation</span></span>

<span data-ttu-id="2de07-103">네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="2de07-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="2de07-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2de07-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2de07-105">는 Pauli Z 기준으로 원하는 비트의 레지스터를 측정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2de07-105">Jointly measures a register of qubits in the Pauli Z basis.</span></span>

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a><span data-ttu-id="2de07-106">Description</span><span class="sxs-lookup"><span data-stu-id="2de07-106">Description</span></span>

<span data-ttu-id="2de07-107">전체 레지스터의 패리티를 표시 하는 $Z \otimes Z \otimes \cst\otimes Z $ 기준으로 stbits의 레지스터를 측정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2de07-107">Measures a register of qubits in the $Z \otimes Z \otimes \cdots \otimes Z$ basis, representing the parity of the entire register.</span></span>

## <a name="input"></a><span data-ttu-id="2de07-108">입력</span><span class="sxs-lookup"><span data-stu-id="2de07-108">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="2de07-109">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="2de07-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="2de07-110">측정할 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="2de07-110">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="2de07-111">출력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="2de07-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="2de07-112">$Z \otimes Z \otimes \cst\otimes Z $를 측정 한 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="2de07-112">The result of measuring $Z \otimes Z \otimes \cdots \otimes Z$.</span></span>