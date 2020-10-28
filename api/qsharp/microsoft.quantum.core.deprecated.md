---
uid: Microsoft.Quantum.Core.Deprecated
title: 사용 되지 않는 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: Deprecated
qsharp.summary: Compiler-recognized attribute used to mark a type or callable as deprecated.
ms.openlocfilehash: b1fcae9647b2a655d25773386ecffa826515516e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713273"
---
# <a name="deprecated-user-defined-type"></a><span data-ttu-id="2f79b-102">사용 되지 않는 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="2f79b-102">Deprecated user defined type</span></span>

<span data-ttu-id="2f79b-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="2f79b-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="2f79b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2f79b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2f79b-105">형식을 표시 하거나 사용 되지 않는 것으로 표시 하는 데 사용 되는 컴파일러 인식 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="2f79b-105">Compiler-recognized attribute used to mark a type or callable as deprecated.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a><span data-ttu-id="2f79b-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="2f79b-106">Named Items</span></span>

### <a name="newname--string"></a><span data-ttu-id="2f79b-107">NewName: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="2f79b-107">NewName : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="2f79b-108">대신 사용할 호출할 수 있는 형식의 전체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f79b-108">The full name of the type or callable to use instead.</span></span>
<span data-ttu-id="2f79b-109">형식 또는 호출 가능이 대체 없이 사용 되지 않는 경우는 빈 문자열로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f79b-109">Is set to the empty String if a type or callable has been deprecated without substitution.</span></span>