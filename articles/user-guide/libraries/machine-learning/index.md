---
title: 양자 기계 학습 패키지 소개 | Microsoft Docs
description: 양자 기계 학습 패키지 소개
author: QuantumWriter
ms.author: alexeib@microsoft.com
ms.date: 12/5/2019
ms.topic: article
uid: microsoft.quantum.machine-learning.concepts.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 2f8884fafd6370e4f70ec93e6fc8617c34c29431
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868851"
---
# <a name="introduction-to-the-quantum-machine-learning-library"></a>양자 기계 학습 라이브러리 소개

Quantum Machine Learning 라이브러리는 Q#으로 작성된 API로, 하이브리드 퀀텀/클래식 기계 학습 실험을 실행하는 기능을 제공합니다. 이 라이브러리는 다음을 수행할 수 있는 기능을 제공합니다.

- 사용자 고유의 데이터를 로드하여 양자 시뮬레이터 분류

- 샘플 및 자습서를 사용하여 양자 기계 학습 분야 학습

현존하는 클래식 기계 학습 프레임워크에 비해 성능이 낮을 것으로 예상할 수 있습니다(이미 컴퓨팅 비용이 많이 드는 양자 디바이스 시뮬레이션을 기반으로 모든 것이 실행되므로).

이 설명서의 목적은 다음과 같습니다.

- 하이브리드 양자/클래식 학습을 위한 기계 학습 도구(Q\#으로 작성)를 간단하게 소개합니다.
- 기계 학습 개념, 특히 양자 회로 중심 분류자(양자 순차 분류자라고도 함)의 실현을 소개합니다.
- 라이브러리에서 제공하는 도구를 사용하기 위한 기본 사항을 알려주는 일련의 자습서를 제공합니다.
- 이러한 분류자의 학습 및 유효성 검사 메서드 및 메서드를 라이브러리에서 제공하는 특정 Q\# 작업으로 변환하는 방법을 설명합니다.

이 라이브러리에 구현된 모델은 [회로 중심 양자 분류자](https://arxiv.org/abs/1804.00633)에 제공되는 양자-클래식 학습 체계를 기반으로 합니다.
