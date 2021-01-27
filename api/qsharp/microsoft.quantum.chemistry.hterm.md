---
uid: Microsoft.Quantum.Chemistry.HTerm
title: HTerm 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTerm
qsharp.summary: Format of data passed from C# to Q# to represent a term of the Hamiltonian. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 744668a4fe96ee00fe2f7991f4e1f05eea19d417
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851779"
---
# <a name="hterm-user-defined-type"></a><span data-ttu-id="ab59e-102">HTerm 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="ab59e-102">HTerm user defined type</span></span>

<span data-ttu-id="ab59e-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="ab59e-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="ab59e-104">패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="ab59e-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="ab59e-105">C #에서 Q #으로 전달 되는 데이터의 형식으로 Hamiltonian의 용어를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ab59e-105">Format of data passed from C# to Q# to represent a term of the Hamiltonian.</span></span>
<span data-ttu-id="ab59e-106">표시 되는 데이터의 의미는 해당 데이터를 수신 하는 알고리즘에 의해 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab59e-106">The meaning of the data represented is determined by the algorithm that receives it.</span></span>

```qsharp

newtype HTerm = (Int[], Double[]);
```

