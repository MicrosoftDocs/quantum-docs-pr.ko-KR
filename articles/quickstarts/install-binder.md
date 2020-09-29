---
title: Q# 및 Binder를 사용하여 개발
description: Binder를 사용하여 Q# 애플리케이션을 만드는 방법을 알아봅니다.
author: bradben
ms.author: v-benbra
ms.date: 9/03/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.binder
no-loc:
- Q#
- $$v
ms.openlocfilehash: f993a1145dd8c01045d4cc7cfd0c98efd574ea78
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90836558"
---
# <a name="develop-with-no-locq-and-binder"></a>Q# 및 Binder를 사용하여 개발

Binder를 사용하여 온라인으로 Jupyter Notebook을 실행하고 공유할 수 있습니다.

## <a name="use-binder-with-the-microsoft-qdk-samples"></a>Microsoft QDK 샘플과 함께 Binder 사용

Microsoft QDK 샘플을 사용하도록 Binder를 자동으로 구성하려면 다음을 수행합니다.

1. 브라우저를 열고 https://aka.ms/try-qsharp 을 실행합니다.
1. **Quantum Development Kit 샘플** 방문 페이지에서 **Q# notebook**을 클릭하여 IQ#을 통해 사용자 고유의 양자 애플리케이션 Notebook을 작성하는 방법을 알아봅니다.

![QDK 방문 페이지](~/media/binder-install.png)

## <a name="use-binder-with-your-own-notebooks-and-repository"></a>사용자 고유의 Notebook 및 리포지토리와 함께 Binder 사용

GitHub 리포지토리에 이미 Notebook이 있는 경우 리포지토리와 함께 작동하도록 Binder를 구성할 수 있습니다.

1. 리포지토리의 루트에 *Dockerfile*이라는 파일이 있는지 확인합니다. 이 파일은 최소한 다음 줄을 포함해야 합니다.

    ```bash
    FROM mcr.microsoft.com/quantum/iqsharp-base:0.12.20082513
    
    USER root
    COPY . ${HOME}
    RUN chown -R ${USER} ${HOME}
    
    USER ${USER}
    ```

    > [!NOTE]
    > [릴리스 정보](xref:microsoft.quantum.relnotes)에서 IQ#의 최신 버전을 확인할 수 있습니다.

    Dockerfile 생성에 대한 자세한 내용은 [Dockerfile 참조](https://docs.docker.com/engine/reference/builder/)를 확인하세요.

2. 브라우저를 열고 [mybinder.org](https://mybinder.org)로 이동합니다.
3. 리포지토리 이름에 **GitHub URL**(예: *MyName/MyRepo*)을 입력하고 **시작**을 클릭합니다.

![MyBinder 양식](~/media/mybinder.png)
    
## <a name="next-steps"></a>다음 단계

이제 Binder 환경을 설정했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성하고 실행할 수 있습니다.
