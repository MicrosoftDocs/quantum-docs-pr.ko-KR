---
uid: Microsoft.Quantum.Canon.Snd
title: Snd 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Snd
qsharp.summary: Given a pair, returns its second element.
ms.openlocfilehash: c05053b45d24c3398526d1269b90bb40d1e0ef27
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715450"
---
# <a name="snd-function"></a><span data-ttu-id="04bec-102">Snd 함수</span><span class="sxs-lookup"><span data-stu-id="04bec-102">Snd function</span></span>

<span data-ttu-id="04bec-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="04bec-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="04bec-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="04bec-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="04bec-105">쌍이 지정 된 경우 두 번째 요소를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="04bec-105">Given a pair, returns its second element.</span></span>

```qsharp
function Snd<'T, 'U> (pair : ('T, 'U)) : 'U
```


## <a name="input"></a><span data-ttu-id="04bec-106">입력</span><span class="sxs-lookup"><span data-stu-id="04bec-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="04bec-107">pair: (' t ', ' U)</span><span class="sxs-lookup"><span data-stu-id="04bec-107">pair : ('T,'U)</span></span>

<span data-ttu-id="04bec-108">두 개의 요소가 포함 된 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="04bec-108">A tuple with two elements.</span></span>



## <a name="output--u"></a><span data-ttu-id="04bec-109">출력: ' U</span><span class="sxs-lookup"><span data-stu-id="04bec-109">Output : 'U</span></span>

<span data-ttu-id="04bec-110">의 두 번째 요소 `pair` 입니다.</span><span class="sxs-lookup"><span data-stu-id="04bec-110">The second element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="04bec-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="04bec-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="04bec-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="04bec-112">'T</span></span>

<span data-ttu-id="04bec-113">쌍의 첫 번째 멤버의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="04bec-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="04bec-114">' U</span><span class="sxs-lookup"><span data-stu-id="04bec-114">'U</span></span>

<span data-ttu-id="04bec-115">쌍의 두 번째 멤버의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="04bec-115">The type of the pair's second member.</span></span>