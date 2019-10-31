---
uid: microsoft.quantum.standardlibsintro
title: 'Microsoft Quantum용 Q # 표준 라이브러리'
description: 'Microsoft Quantum용 Q # 표준 라이브러리에 대한 참조 설명서'
author: natke
ms.author: nakersha
ms.date: 09/04/2019
ms.topic: landing-page
ms.openlocfilehash: 25a53e1cb8577761ef89cdcf2cfcddc509093f86
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2019
ms.locfileid: "72999092"
---
# <a name="q-standard-libraries"></a><span data-ttu-id="fc76d-103">Q# 표준 라이브러리</span><span class="sxs-lookup"><span data-stu-id="fc76d-103">Q# standard libraries</span></span> #

<span data-ttu-id="fc76d-104">Q#은 Q# *표준 라이브러리*를 구성하는 다양한 유용한 연산, 함수 및 사용자 정의 형식에 의해 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc76d-104">Q# is supported by a range of different useful operations, functions, and user-defined types that comprise the Q# *standard library*.</span></span>
<span data-ttu-id="fc76d-105">Q# 표준 라이브러리는 다음 두 가지 주요 부분으로 구분됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc76d-105">The Q# standard library is split into two main parts:</span></span>

- <span data-ttu-id="fc76d-106">**Prelude**: 대상 컴퓨터 및 컴파일러의 일부로 정의된 연산 및 함수로, 일반적으로 클래식 네이티브 .NET 코드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc76d-106">**The prelude**: operations and functions defined as a part of the target machine and compiler, typically in classical native .NET code.</span></span>
  <span data-ttu-id="fc76d-107">일반적으로 대상 컴퓨터마다 각 시스템에 적절하게 다른 Prelude가 구현될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc76d-107">In general, different target machines may have different implementations of the prelude appropriate to each system.</span></span>
- <span data-ttu-id="fc76d-108">**Canon**: Prelude에 정의된 논리를 바탕으로 Q#에 정의되는 연산 및 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="fc76d-108">**The canon**: operations and functions defined in Q# building on the logic defined in the prelude.</span></span>
  <span data-ttu-id="fc76d-109">Canon 구현은 대상 컴퓨터와는 관계가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fc76d-109">The canon implementation is agnostic with respect to target machines.</span></span>
<span data-ttu-id="fc76d-110">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="sxs-lookup"><span data-stu-id="fc76d-110">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span></span>