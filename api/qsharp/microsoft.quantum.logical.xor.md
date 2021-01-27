---
uid: Microsoft.Quantum.Logical.Xor
title: Xor 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Xor
qsharp.summary: Returns the Boolean exclusive disjunction of two values.
ms.openlocfilehash: 4a4af7f628ca64170e046584d9caffe7ceee3d56
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848444"
---
# <a name="xor-function"></a><span data-ttu-id="2de96-102">Xor 함수</span><span class="sxs-lookup"><span data-stu-id="2de96-102">Xor function</span></span>

<span data-ttu-id="2de96-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="2de96-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="2de96-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2de96-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2de96-105">두 값의 부울 배타적 논리합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2de96-105">Returns the Boolean exclusive disjunction of two values.</span></span>

```qsharp
function Xor (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="2de96-106">입력</span><span class="sxs-lookup"><span data-stu-id="2de96-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="2de96-107">a: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2de96-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2de96-108">고려해 야 할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2de96-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="2de96-109">b: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2de96-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2de96-110">고려할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2de96-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="2de96-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2de96-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2de96-112">`true` 및 중 하나만 이면이 고, 그렇지 않으면 `a` `b` `true` 입니다.</span><span class="sxs-lookup"><span data-stu-id="2de96-112">`true` if and only if exactly one of `a` and `b` is `true`.</span></span>