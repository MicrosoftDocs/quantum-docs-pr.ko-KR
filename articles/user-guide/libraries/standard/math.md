---
title: Q#표준 라이브러리의 수학
description: Q#기본 제공 데이터 형식과 함께 사용 되는 표준 라이브러리의 기존 수학 함수에 대해 알아봅니다.
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad
ms.topic: article
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: 6de1574341d67c569cd2f040ec533e263fdd386e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92692056"
---
# <a name="classical-mathematical-functions"></a><span data-ttu-id="b4c29-103">기존 수학 함수</span><span class="sxs-lookup"><span data-stu-id="b4c29-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="b4c29-104">이러한 함수는 Q# 기본 제공 데이터 형식, 및 작업에 주로 사용 됩니다 `Int` `Double` `Range` .</span><span class="sxs-lookup"><span data-stu-id="b4c29-104">These functions are primarily used to work with the Q# built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="b4c29-105"><xref:Microsoft.Quantum.Intrinsic.Random>작업에 시그니처가 `(Double[] => Int)` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4c29-105">The <xref:Microsoft.Quantum.Intrinsic.Random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="b4c29-106">입력으로 double의 배열을 사용 하 고 임의로 선택 된 인덱스를로 배열에 반환 합니다 `Int` .</span><span class="sxs-lookup"><span data-stu-id="b4c29-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="b4c29-107">특정 인덱스를 선택할 확률은 해당 인덱스에 있는 배열 요소의 값에 비례 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c29-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="b4c29-108">0과 같은 n 배열 요소는 무시 되 고 해당 인덱스는 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4c29-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="b4c29-109">배열 요소가 0 보다 작거나 0 보다 큰 배열 요소가 없으면 작업이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c29-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>
