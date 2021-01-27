---
title: Q#표준 라이브러리의 수학
description: Q#기본 제공 데이터 형식과 함께 사용 되는 표준 라이브러리의 기존 수학 함수에 대해 알아봅니다.
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad
ms.topic: conceptual
no-loc:
- Q#
- $$v
ms.openlocfilehash: a2e2656f42213c8ae9e984f63f3ebf4058520532
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853989"
---
# <a name="classical-mathematical-functions"></a>기존 수학 함수 #

이러한 함수는 Q# 기본 제공 데이터 형식, 및 작업에 주로 사용 됩니다 `Int` `Double` `Range` .

<xref:Microsoft.Quantum.Intrinsic.Random>작업에 시그니처가 `(Double[] => Int)` 있습니다.
입력으로 double의 배열을 사용 하 고 임의로 선택 된 인덱스를로 배열에 반환 합니다 `Int` .
특정 인덱스를 선택할 확률은 해당 인덱스에 있는 배열 요소의 값에 비례 합니다. 0과 같은 n 배열 요소는 무시 되 고 해당 인덱스는 반환 되지 않습니다.
배열 요소가 0 보다 작거나 0 보다 큰 배열 요소가 없으면 작업이 실패 합니다.
