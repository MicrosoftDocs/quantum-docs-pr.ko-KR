---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: ExpandedCoefficients 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: 92d7deb7010791e7de3d22ad4616b20110d5e84e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214384"
---
# <a name="expandedcoefficients-function"></a><span data-ttu-id="b9a9a-102">ExpandedCoefficients 함수</span><span class="sxs-lookup"><span data-stu-id="b9a9a-102">ExpandedCoefficients function</span></span>

<span data-ttu-id="b9a9a-103">네임 스페이스: [JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="b9a9a-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="b9a9a-104">패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="b9a9a-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="b9a9a-105">이러한 및 Pauli 용어 사이에 일대일 매핑을 얻기 위해 Jordan-Wigner 계수의 압축 된 표현을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9a9a-105">Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.</span></span>

```qsharp
function ExpandedCoefficients (coeff : Double[], termType : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="b9a9a-106">입력</span><span class="sxs-lookup"><span data-stu-id="b9a9a-106">Input</span></span>

### <a name="coeff--double"></a><span data-ttu-id="b9a9a-107">coeff: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b9a9a-107">coeff : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b9a9a-108">Jordan-Wigner Hamiltonian 데이터 구조에서 읽은 계수의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="b9a9a-108">An array of coefficients, as read from the Jordan-Wigner Hamiltonian data structure.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="b9a9a-109">termType: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b9a9a-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b9a9a-110">Jordan-Wigner 용어의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b9a9a-110">The type of the Jordan-Wigner term.</span></span>



## <a name="output--double"></a><span data-ttu-id="b9a9a-111">Output: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b9a9a-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b9a9a-112">확장 된 계수 배열 (Pauli 용어 당 하나)</span><span class="sxs-lookup"><span data-stu-id="b9a9a-112">Expanded arrays of coefficients, one per Pauli term.</span></span>