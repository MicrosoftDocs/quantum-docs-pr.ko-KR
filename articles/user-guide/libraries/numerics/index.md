---
title: 양자 숫자 라이브러리 소개 | Microsoft Docs
description: 양자 숫자 라이브러리 소개
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: dc6407d9775ad8a401036912abd0b70033796144
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868783"
---
# <a name="introduction-to-the-quantum-numerics-library"></a>양자 숫자 라이브러리 소개

많은 양자 알고리즘은 입력 중첩에 대한 수학 함수를 평가하는 [오라클](xref:microsoft.quantum.concepts.oracles)을 사용합니다.
예를 들어, Shor 알고리즘의 주요 구성 요소는 모든 $2n$비트 문자열에 대한 균일한 중첩에서 고정 $a$, $N$의 인수 및 $x$ a $2n$큐비트 정수에 대해 $f(x) = a^x\operatorname{mod} N$를 계산합니다.

실제 양자 컴퓨터에서 Shor의 알고리즘을 실행하려면 대상 컴퓨터의 네이티브 연산을 기준으로 이 함수를 작성해야 합니다.
최하위 비트에서 계산하는 $i$번째 비트를 나타내는 $x_i$로 $x$의 이진 표현을 나타낼 경우 $f(x)$는 $f(x) = a^{\sum_{i=0}^{2n-1} x_i 2^i} \operatorname{mod} N$로 쓸 수 있습니다.
이 수식을 다시 항 $a^{2^i x_i}=(a^{2^i})^{x_i}$의 product (mod N)으로 쓸 수 있습니다. 따라서 함수 $f(x)$는 $x_i$가 0이 아닌 조건일 때 $2n$ (modular)를 $a^{2^i}$에 곱한 시퀀스를 사용하여 구현할 수 있습니다. 상수 $a^{2^i}$는 알고리즘을 실행하기 전에 미리 계산하여 모듈로 N을 줄일 수 있습니다.

이러한 제어되는 모듈식 곱셈 시퀀스를 다음과 같이 좀 더 간단히 나타낼 수 있습니다. 각 곱셈은 $n$ 제어되는 모듈식 덧셈 시퀀스를 사용하여 수행할 수 있으며, 각 모듈식 덧셈은 일반 덧셈 및 비교 연산자에서 작성할 수 있습니다.


실제 구현에 도달하기 위해서 많은 단계가 필요하다는 가정할 경우, 이러한 함수를 처음부터 사용할 수 있다면 매우 유용할 것입니다.
이때문에 Quantum Development Kit에서는 다양한 범위의 숫자 함수를 지원하고 있습니다.


## <a name="functionality"></a>기능

지금까지 언급한 정수 산술 연산 외에도, 숫자 라이브러리는 다음을 제공합니다.

- 1~2개의 양자 정수를 입력으로 사용하는 부호 있는(없는) 정수 함수(곱하기, 제곱, 나머지 있는 나누기, 역함수, ...)
- 1~2개의 양자 고정 소수점 수를 입력으로 사용하는 고정 소수점 함수(더하기/빼기, 곱하기, 제곱, 1/x, 다항식 계산)

## <a name="getting-started"></a>시작

> [!div class="nextstepaction"]
> [숫자 라이브러리 사용에 대해 알아보기](xref:microsoft.quantum.numerics.usage)
