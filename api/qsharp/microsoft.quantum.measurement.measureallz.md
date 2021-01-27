---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: MeasureAllZ 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: cb3c7cab33efb612bbf5da3b51d2df5d1b8ba1df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854681"
---
# <a name="measureallz-operation"></a><span data-ttu-id="39315-102">MeasureAllZ 작업</span><span class="sxs-lookup"><span data-stu-id="39315-102">MeasureAllZ operation</span></span>

<span data-ttu-id="39315-103">네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="39315-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="39315-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="39315-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="39315-105">는 Pauli Z 기준으로 원하는 비트의 레지스터를 측정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39315-105">Jointly measures a register of qubits in the Pauli Z basis.</span></span>

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a><span data-ttu-id="39315-106">설명</span><span class="sxs-lookup"><span data-stu-id="39315-106">Description</span></span>

<span data-ttu-id="39315-107">전체 레지스터의 패리티를 표시 하는 $Z \otimes Z \otimes \cst\otimes Z $ 기준으로 stbits의 레지스터를 측정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39315-107">Measures a register of qubits in the $Z \otimes Z \otimes \cdots \otimes Z$ basis, representing the parity of the entire register.</span></span>

## <a name="input"></a><span data-ttu-id="39315-108">입력</span><span class="sxs-lookup"><span data-stu-id="39315-108">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="39315-109">register: [](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="39315-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="39315-110">측정할 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="39315-110">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="39315-111">출력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="39315-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="39315-112">$Z \otimes Z \otimes \cst\otimes Z $를 측정 한 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="39315-112">The result of measuring $Z \otimes Z \otimes \cdots \otimes Z$.</span></span>