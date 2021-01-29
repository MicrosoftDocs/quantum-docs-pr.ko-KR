---
title: Q# 및 Binder를 사용하여 개발
description: Binder를 사용하여 Q# 애플리케이션을 만드는 방법을 알아봅니다.
author: bradben
ms.author: v-benbra
ms.date: 9/03/2020
ms.topic: quickstart
uid: microsoft.quantum.install.binder
no-loc:
- Q#
- $$v
ms.openlocfilehash: f7e9b1ae67d6275ec7ba39ea411842dc537536c5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856720"
---
# <a name="develop-with-no-locq-and-binder"></a><span data-ttu-id="4dff5-103">Q# 및 Binder를 사용하여 개발</span><span class="sxs-lookup"><span data-stu-id="4dff5-103">Develop with Q# and Binder</span></span>

<span data-ttu-id="4dff5-104">Binder를 사용하여 온라인으로 Jupyter Notebook을 실행하고 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dff5-104">You can use Binder to run and share your Jupyter Notebooks online.</span></span>

## <a name="use-binder-with-the-microsoft-qdk-samples"></a><span data-ttu-id="4dff5-105">Microsoft QDK 샘플과 함께 Binder 사용</span><span class="sxs-lookup"><span data-stu-id="4dff5-105">Use Binder with the Microsoft QDK samples</span></span>

<span data-ttu-id="4dff5-106">Microsoft QDK 샘플을 사용하도록 Binder를 자동으로 구성하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="4dff5-106">To configure Binder automatically to use the Microsoft QDK samples:</span></span>

1. <span data-ttu-id="4dff5-107">브라우저를 열고 https://aka.ms/try-qsharp 을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4dff5-107">Open a browser and run https://aka.ms/try-qsharp.</span></span>
1. <span data-ttu-id="4dff5-108">**Quantum Development Kit 샘플** 방문 페이지에서 **Q# notebook** 을 클릭하여 IQ#을 통해 사용자 고유의 양자 애플리케이션 Notebook을 작성하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="4dff5-108">On the **Quantum Development Kit Samples** landing page, click **Q# notebook** to learn how to use IQ# to write your own quantum application notebooks.</span></span>

![QDK 방문 페이지](~/media/binder-install.png)

## <a name="use-binder-with-your-own-notebooks-and-repository"></a><span data-ttu-id="4dff5-110">사용자 고유의 Notebook 및 리포지토리와 함께 Binder 사용</span><span class="sxs-lookup"><span data-stu-id="4dff5-110">Use Binder with your own notebooks and repository</span></span>

<span data-ttu-id="4dff5-111">GitHub 리포지토리에 이미 Notebook이 있는 경우 리포지토리와 함께 작동하도록 Binder를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dff5-111">If you already have notebooks in a GitHub repository, you can configure Binder to work with your repo:</span></span>

1. <span data-ttu-id="4dff5-112">리포지토리의 루트에 *Dockerfile* 이라는 파일이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="4dff5-112">Ensure that there is a file named *Dockerfile* in the root of your repository.</span></span> <span data-ttu-id="4dff5-113">이 파일은 최소한 다음 줄을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dff5-113">The file must contain at least the following lines:</span></span>

    ```bash
    FROM mcr.microsoft.com/quantum/iqsharp-base:0.12.20082513
    
    USER root
    COPY . ${HOME}
    RUN chown -R ${USER} ${HOME}
    
    USER ${USER}
    ```

    > [!NOTE]
    > <span data-ttu-id="4dff5-114">[릴리스 정보](xref:microsoft.quantum.relnotes)에서 IQ#의 최신 버전을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dff5-114">You can verify the most current version of IQ# in the [Release Notes](xref:microsoft.quantum.relnotes).</span></span>

    <span data-ttu-id="4dff5-115">Dockerfile 생성에 대한 자세한 내용은 [Dockerfile 참조](https://docs.docker.com/engine/reference/builder/)를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="4dff5-115">For more information about creating a Dockerfile, see the [Dockerfile reference](https://docs.docker.com/engine/reference/builder/).</span></span>

2. <span data-ttu-id="4dff5-116">브라우저를 열고 [mybinder.org](https://mybinder.org)로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="4dff5-116">Open a browser to [mybinder.org](https://mybinder.org).</span></span>
3. <span data-ttu-id="4dff5-117">리포지토리 이름에 **GitHub URL**(예: *MyName/MyRepo*)을 입력하고 **시작** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4dff5-117">Enter your repository name as the **GitHub URL** (for example *MyName/MyRepo*), and click **launch**.</span></span>

![MyBinder 양식](~/media/mybinder.png)
    
## <a name="next-steps"></a><span data-ttu-id="4dff5-119">다음 단계</span><span class="sxs-lookup"><span data-stu-id="4dff5-119">Next steps</span></span>

<span data-ttu-id="4dff5-120">이제 Binder 환경을 설정했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성하고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dff5-120">Now that you have set up your Binder environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
