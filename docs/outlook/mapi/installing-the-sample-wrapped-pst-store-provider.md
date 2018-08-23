---
title: Instalar o provedor do repositório PST encapsulado de exemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: 5b16da68a5cc5ab9e005a262bf1518ea90aac570
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587534"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="2f894-103">Instalar o provedor do repositório PST encapsulado de exemplo</span><span class="sxs-lookup"><span data-stu-id="2f894-103">Installing the Sample Wrapped PST Store Provider</span></span>

  
  
<span data-ttu-id="2f894-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f894-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f894-105">Este tópico leva as etapas para baixar e instalar o provedor de repositórios de PST quebrado automaticamente amostra.</span><span class="sxs-lookup"><span data-stu-id="2f894-105">This topic takes you through the steps to download and install the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="2f894-106">O provedor de repositório PST de quebradas amostra, WrapPST, implementa um provedor de armazenamento com quebra PST que se destina a ser usado em conjunto com a API de replicação.</span><span class="sxs-lookup"><span data-stu-id="2f894-106">The Sample Wrapped PST Store Provider, WrapPST, implements a wrapped PST store provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="2f894-107">Para obter mais informações sobre a API de replicação, consulte [Sobre o API de replicação](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="2f894-107">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="2f894-108">Instale o fornecedor de repositório PST encapsulado da amostra</span><span class="sxs-lookup"><span data-stu-id="2f894-108">Install the Sample Wrapped PST Store Provider</span></span>

1. <span data-ttu-id="2f894-109">Para baixar o provedor de repositórios de PST quebrado automaticamente amostra, consulte [exemplos de código de referência de auxiliar do Outlook 2007 e instalador redistribuível](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="2f894-109">To download the Sample Wrapped PST Store Provider, see [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="2f894-110">Abra a pasta **SampleWrappedPSTStoreProvider** e clique em **Extrair todos os arquivos**.</span><span class="sxs-lookup"><span data-stu-id="2f894-110">Open the **SampleWrappedPSTStoreProvider** folder and click **Extract All Files**.</span></span>
    
3. <span data-ttu-id="2f894-111">Clique em **Procurar**, selecione o local onde deseja salvar a amostra e clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="2f894-111">Click **Browse**, select the location where you want to save the sample, and click **OK**.</span></span>
    
4. <span data-ttu-id="2f894-112">Clique em **extrair**.</span><span class="sxs-lookup"><span data-stu-id="2f894-112">Click **Extract**.</span></span> <span data-ttu-id="2f894-113">A pasta selecionada é exibida e contém os arquivos extraídos.</span><span class="sxs-lookup"><span data-stu-id="2f894-113">The folder you selected appears and contains the extracted files.</span></span>
    
5. <span data-ttu-id="2f894-114">Abra o Visual Studio 2005 como administrador.</span><span class="sxs-lookup"><span data-stu-id="2f894-114">Open Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="2f894-115">Se seu computador estiver executando o Windows XP, você deve ser logado como administrador.</span><span class="sxs-lookup"><span data-stu-id="2f894-115">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="2f894-116">Se seu computador estiver executando o Windows Vista, você deve estar logado como administrador e você deve com o botão direito no ícone do Visual Studio 2005 e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="2f894-116">If your computer is running Windows Vista, you must be logged in as an Administrator and you must right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
6. <span data-ttu-id="2f894-117">No Visual Studio 2005, clique em **arquivo**, selecione **Abrir**e, em seguida, clique em **Project/Solution**.</span><span class="sxs-lookup"><span data-stu-id="2f894-117">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
7. <span data-ttu-id="2f894-118">Navegue até o local onde você salvou a amostra, clique em **WrapPST**e, em seguida, clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="2f894-118">Browse to the location where you saved the sample, click **WrapPST**, and then click **Open**.</span></span>
    
8. <span data-ttu-id="2f894-119">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="2f894-119">On the **Build** menu, click **Build Solution**.</span></span>
    
9. <span data-ttu-id="2f894-120">Na caixa de diálogo **Salvar arquivo como** , clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="2f894-120">In the **Save File As** dialog box, click **Save**.</span></span>
    
10. <span data-ttu-id="2f894-121">Na pasta onde você salvou a amostra, com o botão direito do arquivo **Install. bat** e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="2f894-121">In the folder where you saved the sample, right-click the **Install.bat** file and click **Run as administrator**.</span></span>
    
11. <span data-ttu-id="2f894-122">Na caixa de diálogo **Controle de conta de usuário** , clique em **continuar**.</span><span class="sxs-lookup"><span data-stu-id="2f894-122">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f894-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f894-123">See also</span></span>



[<span data-ttu-id="2f894-124">Sobre o exemplo de provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="2f894-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="2f894-125">Iniciar um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="2f894-125">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="2f894-126">Fazer logon em um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="2f894-126">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="2f894-127">Usar um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="2f894-127">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="2f894-128">Desativar um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="2f894-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

