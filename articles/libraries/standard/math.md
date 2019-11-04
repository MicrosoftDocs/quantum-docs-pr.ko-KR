---
title: 'Q # 표준 라이브러리-수학 | Microsoft Docs'
description: 'Q # 표준 라이브러리-수학'
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: 7ac9d321f59f7cc95ad8939a4cf7c36e0c5e0491
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2019
ms.locfileid: "73184460"
---
# <a name="classical-mathematical-functions"></a>기존 수학 함수 #

이러한 함수는 주로 `Int`, `Double`및 `Range`의 Q # 기본 제공 데이터 형식으로 작업 하는 데 사용 됩니다.

<xref:microsoft.quantum.intrinsic.random> 작업에 `(Double[] => Int)`시그니처가 있습니다.
입력으로 double의 배열을 사용 하 고 임의로 선택 된 인덱스를 `Int`배열로 반환 합니다.
특정 인덱스를 선택할 확률은 해당 인덱스에 있는 배열 요소의 값에 비례 합니다. 0과 같은 n 배열 요소는 무시 되 고 해당 인덱스는 반환 되지 않습니다.
배열 요소가 0 보다 작거나 0 보다 큰 배열 요소가 없으면 작업이 실패 합니다.