---
title: Microsoft QDK 문서에 기여
description: Microsoft 퀀텀 설명서 집합에 개념 또는 API 콘텐츠를 참여 하는 방법에 대해 알아봅니다.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.docs
ms.openlocfilehash: ed5ab5df9de5d71ccd922cd430cf15779806dd6a
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275497"
---
# <a name="improving-documentation"></a>설명서 개선

퀀텀 개발 키트에 대 한 설명서는 퀀텀 개발자가 정보를 쉽게 사용할 수 있도록 여러 가지 형태를 사용 합니다.

[코드와 같은 문서](https://www.writethedocs.org/guide/docs-as-code/)원칙에 따라 모든 퀀텀 개발 키트 설명서는 코드로 형식이 지정 되 고, Git를 사용 하 여 Git를 사용 하 여 관리 됩니다 .이는 퀀텀 개발 키트를 빌드하는 데 사용 되는 소스 코드와 동일 합니다.
대부분의 경우 코드 지원 설명서는 다양 한 형식의 [Markdown](https://daringfireball.net/projects/markdown/)로 구성 되며, 명령줄, ide 및 소스 제어에서 사용 하기 쉬운 일반 텍스트 형식으로 다양 한 형식의 텍스트를 작성 하는 데 사용 되는 언어입니다.
이와 비슷한 방식으로 [MathJax](https://www.mathjax.org/) 라이브러리를 채택 하 여 아래에서 설명 하는 것 처럼 LaTeX 언어를 사용 하는 설명서에서 수학 형식을 지정할 수 있습니다.


즉, 각 설명서 형태는 세부 정보에서 약간 다릅니다.

- **개념 설명서** 는에 게시 되는 일련의 문서를 구성 https://docs.microsoft.com/quantum 하며,이를 통해 퀀텀 컴퓨팅의 기본 사항에서 교환 형식에 대 한 기술 사양을 설명 하는 모든 것을 설명 합니다. 이러한 문서는 풍부한 설명서 집합을 만드는 데 사용 되는 Markdown variant 인 [Flavored Markdown (DFM)](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html)로 작성 되었습니다.
- **API 참조** 는에 게시 된 각 Q # 함수, 작업 및 사용자 정의 형식에 대 한 페이지 집합입니다 https://docs.microsoft.com/qsharp/api/ . 이러한 페이지에는 호출 가능한 각에 대 한 입력 및 작업과 추가 정보에 대 한 링크와 예제가 나와 있습니다. API 참조는 각 릴리스의 일부로 Q # 소스 코드의 small DFM 문서에서 자동으로 추출 됩니다.
- 각 샘플 및 kata에 포함 된 **추가 정보 <!----> ** 파일은 해당 샘플 또는 kata를 사용 하는 방법, 포함 된 내용, 나머지 퀀텀 개발 키트와의 관계를 설명 합니다. 이러한 파일은 코드 리포지토리에 직접 문서를 연결 하는 데 널리 사용 되는 [DFM (GitHub Flavored Markdown)](https://github.github.com/gfm/)을 사용 하 여 작성 되었습니다.

## <a name="contributing-to-the-conceptual-documentation"></a>개념 설명서에 기여

개념 또는 추가 정보 설명서에 대 한 향상 된 기능을 제공 하기 위해은 적절 하 게 [**MicrosoftDocs/양자**](https://github.com/MicrosoftDocs/quantum-docs-pr/
), [**microsoft/퀀텀**](https://github.com/Microsoft/Quantum)또는 [**microsoft/QuantumKatas**](https://github.com/Microsoft/QuantumKatas)로 끌어오기 요청을 시작 합니다.
아래의 끌어오기 요청에 대해 자세히 설명 하겠습니다. 지금은 설명서를 개선 하는 데 도움이 되는 몇 가지 사항이 있습니다.

- 독자는 매우 광범위 한 배경에서 퀀텀 개발 키트 설명서를 제공 합니다. 퀀텀 컴퓨팅 연구를 수행 하는 있었던 교직원에 게 새롭고 흥미로운 작업을 배우는 학교 학생의 모든 사람들은 설명서를 읽을 수 있습니다. 가능 하면 판독기의 일부에 대 한 광범위 한 정보를 생각해 서는 안 됩니다. 이는 명확 하 고 액세스 가능한 설명을 제공 하거나 자세한 정보를 위해 다른 리소스에 대 한 링크를 제공할 수 있는 경우에 가장 유용 합니다.
- 설명서 집합은 설명서 나 문서와 같이 배치 되지 않으며, 독자가 "중간" 처럼 보일 수도 있습니다. 예를 들어 검색 엔진은 인덱스를 제안 하지 않을 수도 있고, 친구가 링크를 전송 하 여 도움을 받을 수도 있습니다. 적절 한 링크와 함께 명확한 컨텍스트를 항상 제공 하 여 판독기를 도와 보세요.
- 일부 판독기는 가장 유용 하 게 사용할 수 있는 추상 문과 정의를 찾을 수 있는 반면, 다른 독자는 구체적 예제에서 추정 가장 잘 작동 합니다. 일반적인 사례와 특정 예제를 모두 제공 하면 두 판독기 모두 퀀텀 프로그래밍을 최대한 활용할 수 있습니다.
- 특히 문서화 되는 코드를 작성 한 경우 독자에 게 명확 하지 않은 것을 알 수 있습니다. 한 가지 고유한 프로그램을 프로그래밍 방식으로 사용할 수 있는 것은 아닙니다. 즉, 독자가 무엇 인지에 관계 없이 코드에서 아이디어를 표현 하는 데 가장 유용한 디자인 패턴을 추측할 수 없습니다. 판독기가 코드를 사용할 수 있도록 하는 방법에 대 한 자세한 내용은 해당 컨텍스트를 제공 하는 데 도움이 될 수 있습니다.
- 퀀텀 프로그래밍 커뮤니티의 많은 멤버는 교육 연구원 이며 주로 커뮤니티에 대 한 기여에 대 한 인용문을 통해 인식 됩니다. 독자 들이 추가 자료를 쉽게 찾을 수 있도록 하는 것 외에도, 용지, 통신, 블로그 게시물 및 소프트웨어 도구와 같은 교육용 자료를 적절히 명시 하 여 교육 참가자가 커뮤니티를 개선 하는 데 가장 적합 한 작업을 유지할 수 있습니다.
- 퀀텀 프로그래밍 커뮤니티는 광범위 하 고 wonderfully 다양 한 커뮤니티입니다. 세 번째 사용자 예의 gendered 대명사 (예: "사용자 ..., he ...")를 사용 하는 것은 포함이 아닌 제외 작업에 사용할 수 있습니다. 인용 및 링크에서 사람들의 이름을 cognizant, 비 ASCII 문자를 올바르게 포함 하는 경우 해당 멤버에 대 한 내용을 표시 하 여 커뮤니티의 다양성을 제공할 수 있습니다. 마찬가지로, 영어 언어의 많은 단어는 기술 설명서에서 사용 하는 경우 개별 판독기와 커뮤니티 모두에 게 피해를 일으킬 수 있습니다.

### <a name="referencing-sample-code-from-conceptual-articles"></a>개념 문서에서 샘플 코드 참조

[샘플 리포지토리의](https://github.com/Microsoft/Quantum)코드를 포함 하려면 특수 Docfx-Flavored Markdown 명령을 사용 하 여이 작업을 수행할 수 있습니다.

```markdown
:::code language="qsharp" source="~/quantum/samples/algorithms/chsh-game/Game.qs" range="4-8":::
```

이 명령은 [ `Game.qs` `chsh-game` 샘플에서 파일](https://github.com/microsoft/Quantum/blob/master/samples/algorithms/chsh-game/Game.qs)의 4 ~ 8 줄을 가져와 구문 강조 표시를 위해 Q # 코드로 표시 합니다.
이 명령을 사용 하면 설명서의 샘플 코드를 항상 최대한 최신 상태로 유지 하기 위해 개념 아티클과 샘플 리포지토리 간에 코드를 복제할 수 있습니다.

## <a name="contributing-to-the-api-references"></a>API 참조에 기여

API 참조에 대 한 향상 된 기능을 제공 하기 위해 문서화 되는 코드에서 직접 끌어오기 요청을 여는 것이 가장 유용 합니다.
각 함수, 작업 또는 사용자 정의 형식은 문서 주석을 지원 합니다 (대신로 표시 됨 `///` `//` ).
퀀텀 개발 키트의 각 릴리스를 컴파일할 때 이러한 주석은 https://docs.microsoft.com/qsharp/api/ 각 호출의 입력 및 출력에 대 한 세부 정보, 호출할 수 있는 각각의 가정 및 사용 방법에 대 한 예제를 포함 하 여에 대 한 API 참조를 생성 하는 데 사용 됩니다.

> [!IMPORTANT]
> 이러한 파일은 각각의 새 릴리스로 덮어쓰므로 생성 된 API 설명서를 수동으로 편집 하지 마십시오.
> 우리는 커뮤니티에 대 한 기여를 제공 하 고 변경 내용이 릴리스 후 사용자의 릴리스를 계속 하는 데 도움이 되도록 합니다.

예를 들어 함수를 살펴보겠습니다 `ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)` .
설명서 주석은 사용자가 및 함수를 해석 하는 방법을 이해 하는 데 도움이 됩니다 `bits` `oracle` .
이러한 각 정보는 설명서 주석에서 특수 하 게 명명 된 Markdown 섹션에 의해 Q # 컴파일러에 제공 될 수 있습니다.
예를 들어 `ControlledOnBitString` 다음과 같은 항목을 작성할 수 있습니다.

```qsharp
 /// # Summary
 /// Returns a unitary operation that applies an oracle on the target register if the 
 /// control register state corresponds to a specified bit mask.
 ///
 /// # Description
 /// The output of this function is an operation that can be represented by a
 /// unitary transformation $U$ such that
 /// \begin{align}
 ///     U \ket{b_0 b_1 \cdots b_{n - 1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_{n-1}} \otimes
 ///     \begin{cases}
 ///         V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_{n - 1}) = \texttt{bits} \\\\
 ///         \ket{\psi} & \textrm{otherwise}
 ///     \end{cases},
 /// \end{align}
 /// where $V$ is a unitary transformation that represents the action of the
 /// `oracle` operation.
 ///
 /// # Input
 /// ## bits
 /// The bit string to control the given unitary operation on.
 /// ## oracle
 /// The unitary operation to be applied on the target register.
 ///
 /// # Output
 /// A unitary operation that applies `oracle` on the target register if the control 
 /// register state corresponds to the bit mask `bits`.
 ///
 /// # Remarks
 /// The length of `bits` and `controlRegister` must be equal.
 ///
 /// Given a Boolean array `bits` and a unitary operation `oracle`, the output of this function
 /// is an operation that performs the following steps:
 /// * apply an `X` operation to each qubit of the control register that corresponds to `false` 
 /// element of the `bits`;
 /// * apply `Controlled oracle` to the control and target registers;
 /// * apply an `X` operation to each qubit of the control register that corresponds to `false` 
 /// element of the `bits` again to return the control register to the original state.
 ///
 /// The output of the `Controlled` functor is a special case of `ControlledOnBitString` where `bits` is equal to `[true, ..., true]`.
 ///
 /// # Example
 /// The following code snippets are equivalent:
 /// ```qsharp
 /// (ControlledOnBitString(bits, oracle))(controlRegister, targetRegister);
 /// ```
 /// and
 /// ```qsharp
 /// within {
 ///     ApplyPauliFromBitString(PauliX, false, bits, controlRegister);
 /// } apply {
 ///     Controlled oracle(controlRegister, targetRegister);
 /// }
 /// ```
 ///
 /// The following code prepares a state $\frac{1}{2}(\ket{00} - \ket{01} + \ket{10} + \ket{11})$:
 /// ```qsharp
 /// using (register = Qubit[2]) {
 ///     ApplyToEach(H, register);
 ///     (ControlledOnBitString([false], Z))(register[0..0], register[1]);
 /// }
 /// ```
 function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
 {
     return ControlledOnBitStringImpl(bits, oracle, _, _);
 }
```

[ `ControlledOnBitString` 함수에 대 한 API 설명서](xref:microsoft.quantum.canon.controlledonbitstring)에서 위의 코드에 대해 렌더링 된 버전을 볼 수 있습니다.

문서 작성에 대 한 일반적인 관행 외에도 API 문서 주석을 작성 하면 몇 가지 사항을 염두에 두어야 합니다.

- 각 문서 주석의 형식은 Q # 컴파일러에서 설명서가 올바르게 표시 될 것으로 예상 하는 내용과 일치 해야 합니다. 예를 들어, 일부 섹션 `/// # Remarks` 은 자유형 콘텐츠를 허용 하지만 섹션과 같은 섹션 `/// # See Also` 은 더 제한적입니다.
- 판독기는 주 API 참조 사이트, 각 네임 스페이스에 대 한 요약 또는 가리키기 정보를 사용 하 여 IDE 내 에서도 API 설명서를 읽을 수 있습니다. `/// # Summary`문장에 대 한 보다 길지 않으면 판독기가 더 많은 부분을 읽고 있는지 확인 하 고 네임 스페이스 요약을 통해 신속 하 게 검색 하는 데 도움이 될 수 있습니다.
- 설명서가 코드 자체 보다 훨씬 더 오래 걸릴 수 있지만이는 정상입니다. 코드가 존재 하는 컨텍스트를 모르는 사용자에 게 예기치 않은 결과가 발생할 수 있습니다. 구체적인 예제와 명확한 설명을 제공 하 여 사용자가 사용할 수 있는 코드를 최대한 활용할 수 있도록 도와 줍니다.

<!-- ## LaTeX Formatting ##

**TODO** -->
