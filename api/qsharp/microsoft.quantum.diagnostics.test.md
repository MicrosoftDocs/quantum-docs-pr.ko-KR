---
uid: Microsoft.Quantum.Diagnostics.Test
title: 사용자 정의 형식 테스트
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Test
qsharp.summary: Compiler-recognized attribute used to mark a unit test.
ms.openlocfilehash: 80821cb46d773d84085838d9ee539a8a45c43e61
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201498"
---
# <a name="test-user-defined-type"></a>사용자 정의 형식 테스트

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


단위 테스트를 표시 하는 데 사용 되는 컴파일러 인식 특성입니다.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Test = (ExecutionTarget : String);
```



## <a name="named-items"></a>명명 된 항목

### <a name="executiontarget--string"></a>ExecutionTarget: [문자열](xref:microsoft.quantum.lang-ref.string)

