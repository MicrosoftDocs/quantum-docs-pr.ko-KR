---
title: Microsoft Quantum Development Kit 참여
description: Microsoft Quantum Development Kit 및 양자 개발 커뮤니티에 참여하는 방법을 알아봅니다.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing
ms.openlocfilehash: cf913a09395f0694a51645ec8f91171e5b1555c3
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/10/2020
ms.locfileid: "79022471"
---
# <a name="contributing-to-the-quantum-development-kit"></a>Quantum Development Kit 참여

Quantum Development Kit는 양자 프로그램을 작성하기 위한 도구 모음 그 이상입니다.
양자 컴퓨팅을 검색하고, 양자 알고리즘에서 연구를 수행하고, 양자 디바이스에 대한 새 애플리케이션을 개발하고, 양자 프로그래밍을 최대한 활용하기 위해 작업하는 광범위한 사용자 커뮤니티의 일부입니다.
이 커뮤니티의 멤버인 Quantum Development Kit는 다양한 배경을 지닌 양자 개발자들에게 필요한 기능을 제공하는 것을 목표로 합니다.
Quantum Development Kit에 참여하면 다른 양자 개발자가 사용하는 도구, 이러한 도구를 문서화하는 방법 및 전체 양자 프로그래밍 커뮤니티를 더 나은 검색 및 생성 환경으로 만드는 데 도움이 되는 새로운 기능을 구축하여 이러한 목표를 달성하는 데 기여할 수 있습니다.
당사는 여러분의 자발적인 참여에 매우 감사드리며 당사 커뮤니티의 발전에 참여할 수 있는 기회를 드리고자 합니다.

이 가이드에서는 점점 더 확장되고 있는 양자 프로그래밍 커뮤니티에 기여하는 방법을 설명합니다.

## <a name="building-community"></a>커뮤니티 구축

참여하는 첫 번째 방법은 참여하려는 커뮤니티를 항상 염두에 두는 것입니다.
양자 프로그래밍 커뮤니티의 동료들을 존중함으로써 사용자를 환영하는 최고의 커뮤니티가 되도록 도움을 주실 수 있습니다.

이러한 노력의 일환으로, 모든 Quantum Development Kit 프로젝트는 [Microsoft 오픈 소스 준수 사항](https://opensource.microsoft.com/codeofconduct/)을 채택했습니다.
자세한 내용은 [준수 사항 FAQ](https://opensource.microsoft.com/codeofconduct/faq/)를 참조하거나 [opencode@microsoft.com](mailto:opencode@microsoft.com)에 추가 질문 또는 의견을 알려주세요.

## <a name="what-kinds-of-contributions-help-the-community"></a>커뮤니티에 도움이 되는 참여 유형에는 어떤 것이 있나요?

참여를 통해 양자 프로그래밍 커뮤니티에 도움을 주는 다양한 방법이 있습니다.
이 가이드에서는 특히 Quantum Development Kit와 관련된 세 가지 방법을 집중적으로 설명합니다.
이러한 모든 방법은 사용자를 지원하는 양자 커뮤니티를 구축하는 데 매우 중요합니다.
즉, 완전한 목록은 아니며, 커뮤니티의 양자 프로그래밍 구현을 지원하는 데 도움이 되는 다른 방법들도 알아볼 수 있습니다.

- **버그 보고.** 버그 및 다른 종류의 문제를 해결하는 첫 번째 단계는 해당 버그를 파악하는 것입니다. Quantum Development Kit에서 버그를 발견한 경우 이를 수정하여 양자 프로그래밍 커뮤니티를 위한 더 나은 도구 세트를 개발할 수 있도록 알려주세요.
- **설명서 개선.** 모든 설명서 세트는 보다 자세한 정보를 포함하고 접근이 용이하도록 항상 개선할 수 있습니다.
- **코드 기여.** 물론, 가장 직접적인 참여 방법은 Quantum Development Kit에 새 코드를 추가하는 것입니다.

이러한 종류의 참여는 모두 매우 유용하며 큰 도움이 됩니다.
이 가이드의 나머지 부분에서는 각 유형의 참여를 수행하는 방법에 대한 권장 지침을 제공합니다.

## <a name="where-do-contributions-go"></a>기여한 데이터는 어디로 이동되나요?

Quantum Development Kit에는 양자 프로그램을 작성하기 위한 플랫폼을 실현하기 위해 유기적으로 작용하는 다양한 부분이 포함되어 있습니다.
이러한 각 부분은 다른 리포지토리에 해당되므로 초기에 각 기여 데이터가 속할 가장 적합한 위치를 구분하게 됩니다.

- [**microsoft/양자**](https://github.com/Microsoft/Quantum): Quantum Development Kit를 시작하는 데 도움이 되는 샘플 및 도구입니다.
- [**microsoft/QuantumLibraries**](https://github.com/Microsoft/QuantumLibraries): Quantum Development Kit의 표준 및 도메인별 라이브러리입니다.
- [**microsoft/QuantumKatas**](https://github.com/Microsoft/QuantumKatas): 양자 컴퓨팅 및 Q# 프로그래밍 언어를 학습하기 위한 자기 주도적 프로그래밍 연습 과정입니다.
- [**microsoft/qsharp-compiler**](https://github.com/microsoft/qsharp-compiler): Q# 컴파일러, Visual Studio 확장 및 Visual Studio Code 확장입니다.
- [**microsoft/qsharp-runtime**](https://github.com/microsoft/qsharp-runtime): Quantum Development Kit용 시뮬레이션 프레임워크, 코드 생성 및 시뮬레이션 대상 컴퓨터입니다.
- [**microsoft/iqsharp**](https://github.com/microsoft/iqsharp): 클라우드 환경에서 IQ#을 사용하기 위한 Docker 이미지와 Q#용 jupyter 커널 및 Python 호스트 기능입니다.
- [**MicrosoftDocs/quantum-docs-pr**](https://github.com/MicrosoftDocs/quantum-docs-pr): https://docs.microsoft.com/quantum 에서 게시된 설명서의 소스 코드입니다.

> [!NOTE]
> 죄송하지만 지금은 [**microsoft/Quantum-NC**](https://github.com/microsoft/Quantum-NC) 리포지토리의 코드 및 설명서에 참여하실 수 없습니다. 그렇지만 보내주시는 버그 보고서를 감사히 사용하고 있습니다.

다른 이벤트 또는 Quantum Development Kit와 관련된 보조 기능에 초점을 맞춘 몇 가지 기타 특수한 리포지토리가 더 있습니다.

- [**msr-quarc/qsharp.sty**](https://github.com/msr-quarc/qsharp.sty): Q# 구문에 대한 LaTeX 형식 지원입니다.
- [**msr-quarc/intern-workshop-2019**](https://github.com/msr-quarc/intern-workshop-2019): 2019년 임시 워크샵에서 제공된 Deutsch–Jozsa 자습서용 IQ# Notebook입니다.

## <a name="next-steps"></a>다음 단계

Quantum Development Kit 커뮤니티에 참여해 주셔서 감사합니다.
참여 방법에 대한 자세한 내용을 보려면 다음 가이드 중 하나를 계속 참조하세요.

> [!div class="nextstepaction"]
> [버그를 보고하는 방법 알아보기](xref:microsoft.quantum.contributing.reporting)

> [!div class="nextstepaction"]
> [설명서에 기여하는 방법 알아보기](xref:microsoft.quantum.contributing.docs)

> [!div class="nextstepaction"]
> [끌어오기 요청을 여는 방법 알아보기](xref:microsoft.quantum.contributing.pulls)
