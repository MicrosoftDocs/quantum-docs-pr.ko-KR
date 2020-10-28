---
uid: Microsoft.Quantum.Diagnostics.Test
title: 사용자 정의 형식 테스트
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Test
qsharp.summary: Compiler-recognized attribute used to mark a unit test.
ms.openlocfilehash: 8030f6378ac0cb393c7ed2b9e636a7561e8943a4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712643"
---
# <a name="test-user-defined-type"></a><span data-ttu-id="fe206-102">사용자 정의 형식 테스트</span><span class="sxs-lookup"><span data-stu-id="fe206-102">Test user defined type</span></span>

<span data-ttu-id="fe206-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="fe206-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="fe206-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fe206-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fe206-105">단위 테스트를 표시 하는 데 사용 되는 컴파일러 인식 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="fe206-105">Compiler-recognized attribute used to mark a unit test.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Test = (ExecutionTarget : String);
```



## <a name="named-items"></a><span data-ttu-id="fe206-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="fe206-106">Named Items</span></span>

### <a name="executiontarget--string"></a><span data-ttu-id="fe206-107">ExecutionTarget: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="fe206-107">ExecutionTarget : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

