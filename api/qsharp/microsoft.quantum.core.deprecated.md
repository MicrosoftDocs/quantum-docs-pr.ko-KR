---
uid: Microsoft.Quantum.Core.Deprecated
title: 사용 되지 않는 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: Deprecated
qsharp.summary: Compiler-recognized attribute used to mark a type or callable as deprecated.
ms.openlocfilehash: 1a32d98f5d034c2673d42301b45379da1302ca7f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98832080"
---
# <a name="deprecated-user-defined-type"></a>사용 되지 않는 사용자 정의 형식

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Core)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


형식을 표시 하거나 사용 되지 않는 것으로 표시 하는 데 사용 되는 컴파일러 인식 특성입니다.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a>명명 된 항목

### <a name="newname--string"></a>NewName: [문자열](xref:microsoft.quantum.lang-ref.string)

대신 사용할 호출할 수 있는 형식의 전체 이름입니다.
형식 또는 호출 가능이 대체 없이 사용 되지 않는 경우는 빈 문자열로 설정 됩니다.