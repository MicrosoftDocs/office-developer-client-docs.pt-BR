---
title: Exemplo de provedor de repositório de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 25c606531aa9a7436306a1b87c32aab49fd975db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593911"
---
# <a name="message-store-provider-sample"></a><span data-ttu-id="9bee1-103">Exemplo de provedor de repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="9bee1-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="9bee1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bee1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bee1-105">O provedor de repositórios de PST quebrado automaticamente amostra usa um provedor de pastas particulares (. PST) do arquivo como back-end para armazenar os dados.</span><span class="sxs-lookup"><span data-stu-id="9bee1-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="9bee1-106">O provedor de repositórios de PST com quebra deve ser usado em conjunto com a API de replicação.</span><span class="sxs-lookup"><span data-stu-id="9bee1-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="9bee1-107">A API de replicação permite que você replique os itens de um repositório de dados back-end em um repositório de PST do Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="9bee1-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="9bee1-108">Você pode usar a API de replicação para replicar os dados para um repositório de PST dedicado e controlar o estado de sincronização.</span><span class="sxs-lookup"><span data-stu-id="9bee1-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="9bee1-109">Para obter mais informações, consulte [Sobre o API de replicação](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="9bee1-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="9bee1-110">A maioria das funções do provedor de armazenamento do exemplo quebradas PST passa seus argumentos diretamente para o provedor de PST subjacente.</span><span class="sxs-lookup"><span data-stu-id="9bee1-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="9bee1-111">Determinadas funções exigem implementação especial e são descritas nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="9bee1-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9bee1-112">Executável:</span><span class="sxs-lookup"><span data-stu-id="9bee1-112">Executable:</span></span>  <br/> |<span data-ttu-id="9bee1-113">WrpPST32.dll</span><span class="sxs-lookup"><span data-stu-id="9bee1-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="9bee1-114">Diretório de origem do código:</span><span class="sxs-lookup"><span data-stu-id="9bee1-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="9bee1-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="9bee1-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="9bee1-116">Idioma:</span><span class="sxs-lookup"><span data-stu-id="9bee1-116">Language:</span></span>  <br/> |<span data-ttu-id="9bee1-117">C++</span><span class="sxs-lookup"><span data-stu-id="9bee1-117">C++</span></span>  <br/> |
|<span data-ttu-id="9bee1-118">Plataformas:</span><span class="sxs-lookup"><span data-stu-id="9bee1-118">Platforms:</span></span>  <br/> |<span data-ttu-id="9bee1-119">Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="9bee1-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="9bee1-120">Recursos compatíveis</span><span class="sxs-lookup"><span data-stu-id="9bee1-120">Supported Features</span></span>

<span data-ttu-id="9bee1-121">Esta amostra suporta o Microsoft Outlook 2010 64-bit e agora foi revisada para o Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="9bee1-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="9bee1-122">Consulte os tópicos a seguir para obter informações adicionais:</span><span class="sxs-lookup"><span data-stu-id="9bee1-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="9bee1-123">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="9bee1-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="9bee1-124">Iniciar um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="9bee1-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="9bee1-125">Fazer logon em um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="9bee1-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="9bee1-126">Usar um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="9bee1-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="9bee1-127">Desativar um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="9bee1-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="9bee1-128">**Para instalar o provedor de armazenamento do exemplo quebradas PST**</span><span class="sxs-lookup"><span data-stu-id="9bee1-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="9bee1-129">Para baixar o provedor de PST quebrado automaticamente da amostra, consulte [Baixando as amostras de MAPI do Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="9bee1-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="9bee1-130">Localize a pasta onde você salvou as amostras de MAPI do Outlook.</span><span class="sxs-lookup"><span data-stu-id="9bee1-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="9bee1-131">Com o botão direito do **OutlookMAPISamples -\<número da versão\> ** zip pasta e clique em **Extrair tudo**.</span><span class="sxs-lookup"><span data-stu-id="9bee1-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="9bee1-132">Clique em **Procurar**, selecione o local onde deseja salvar a amostra e, em seguida, clique em **extrair**.</span><span class="sxs-lookup"><span data-stu-id="9bee1-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="9bee1-133">Execute o Microsoft Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="9bee1-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="9bee1-134">No Microsoft Visual Studio 2008, clique em **arquivo**, selecione **Abrir**e, em seguida, clique em **Project/Solution**.</span><span class="sxs-lookup"><span data-stu-id="9bee1-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="9bee1-135">Navegue até o local onde você salvou a amostra, clique em **WrapPST.vcproj**e, em seguida, clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="9bee1-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="9bee1-136">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="9bee1-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="9bee1-137">Na caixa de diálogo **Salvar arquivo como** , clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="9bee1-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="9bee1-138">Na pasta onde você salvou a amostra, com o botão direito do arquivo **Install. bat** e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="9bee1-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="9bee1-139">Na caixa de diálogo **Controle de conta de usuário** , clique em **continuar**.</span><span class="sxs-lookup"><span data-stu-id="9bee1-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    

