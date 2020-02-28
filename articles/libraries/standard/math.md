---
title: 'Q # 표준 라이브러리의 수학'
description: '기본 제공 데이터 형식과 함께 사용 되는 Q # 표준 라이브러리의 기존 수학 함수에 대해 알아봅니다.'
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: bec866472abc0d4327cdc570306341375395f492
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906154"
---
# <a name="classical-mathematical-functions"></a><span data-ttu-id="577bf-103">기존 수학 함수</span><span class="sxs-lookup"><span data-stu-id="577bf-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="577bf-104">이러한 함수는 주로 `Int`, `Double`및 `Range`의 Q # 기본 제공 데이터 형식으로 작업 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="577bf-104">These functions are primarily used to work with the Q# built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="577bf-105"><xref:microsoft.quantum.intrinsic.random> 작업에 `(Double[] => Int)`시그니처가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="577bf-105">The <xref:microsoft.quantum.intrinsic.random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="577bf-106">입력으로 double의 배열을 사용 하 고 임의로 선택 된 인덱스를 `Int`배열로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="577bf-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="577bf-107">특정 인덱스를 선택할 확률은 해당 인덱스에 있는 배열 요소의 값에 비례 합니다.</span><span class="sxs-lookup"><span data-stu-id="577bf-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="577bf-108">0과 같은 n 배열 요소는 무시 되 고 해당 인덱스는 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="577bf-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="577bf-109">배열 요소가 0 보다 작거나 0 보다 큰 배열 요소가 없으면 작업이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="577bf-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>
