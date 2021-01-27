---
uid: Microsoft.Quantum.Diagnostics.Test
title: 사용자 정의 형식 테스트
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Test
qsharp.summary: Compiler-recognized attribute used to mark a unit test.
ms.openlocfilehash: 2f1b521c4ef2bf8e672ca4fe7a5f380d744300b7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853266"
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

