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
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436864"
---
# <a name="message-store-provider-sample"></a><span data-ttu-id="4d3cf-103">Exemplo de provedor de repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="4d3cf-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="4d3cf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d3cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d3cf-105">O exemplo de provedor de repositório PST encapsulado usa um provedor de arquivos de pastas particulares (PST) como back-end para armazenar dados.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="4d3cf-106">O provedor de repositório PST encapsulado deve ser usado em conjunto com a API de replicação.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="4d3cf-107">A API de replicação permite que você replique itens de um repositório de dados de back-end para um repositório de PST do Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="4d3cf-108">Use a API de replicação para replicar os dados em um repositório PST dedicado e manter o controle do estado de sincronização.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="4d3cf-109">Para obter mais informações, consulte [sobre a API de replicação](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="4d3cf-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="4d3cf-110">A maioria das funções no provedor de repositório PST encapsulado de amostra passam seus argumentos diretamente para o provedor de PST subjacente.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="4d3cf-111">Determinadas funções exigem implementação especial e são descritos nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4d3cf-112">Arquivo</span><span class="sxs-lookup"><span data-stu-id="4d3cf-112">Executable:</span></span>  <br/> |<span data-ttu-id="4d3cf-113">WrpPST32. dll</span><span class="sxs-lookup"><span data-stu-id="4d3cf-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="4d3cf-114">Diretório do código-fonte:</span><span class="sxs-lookup"><span data-stu-id="4d3cf-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="4d3cf-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="4d3cf-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="4d3cf-116">Pacote</span><span class="sxs-lookup"><span data-stu-id="4d3cf-116">Language:</span></span>  <br/> |<span data-ttu-id="4d3cf-117">C++</span><span class="sxs-lookup"><span data-stu-id="4d3cf-117">C++</span></span>  <br/> |
|<span data-ttu-id="4d3cf-118">Plataformas</span><span class="sxs-lookup"><span data-stu-id="4d3cf-118">Platforms:</span></span>  <br/> |<span data-ttu-id="4d3cf-119">Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="4d3cf-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="4d3cf-120">Recursos com suporte</span><span class="sxs-lookup"><span data-stu-id="4d3cf-120">Supported Features</span></span>

<span data-ttu-id="4d3cf-121">Este exemplo suporta o Microsoft Outlook 2010 64-bit e foi revisado para o Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="4d3cf-122">Consulte os tópicos a seguir para obter informações adicionais:</span><span class="sxs-lookup"><span data-stu-id="4d3cf-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="4d3cf-123">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="4d3cf-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="4d3cf-124">Inicializando um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="4d3cf-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="4d3cf-125">Fazer logon em um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="4d3cf-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="4d3cf-126">Usando um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="4d3cf-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="4d3cf-127">DesLigamento de um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="4d3cf-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="4d3cf-128">**Para instalar o exemplo de provedor de repositório PST encapsulado**</span><span class="sxs-lookup"><span data-stu-id="4d3cf-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="4d3cf-129">Para baixar o exemplo de provedor de PST encapsulado, confira [download dos exemplos de MAPI do Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="4d3cf-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="4d3cf-130">Localize a pasta onde você salvou os exemplos de MAPI do Outlook.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="4d3cf-131">Clique com o botão direito do mouse na pasta zip **OutlookMAPISamples número\<\> de versão** e clique em **extrair tudo**.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="4d3cf-132">Clique em **procurar**, selecione o local onde deseja salvar o exemplo e, em seguida, clique em **extrair**.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="4d3cf-133">Execute o Microsoft Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="4d3cf-134">No Microsoft Visual Studio 2008, clique em **arquivo**, selecione **abrir**e, em seguida, clique em **projeto/solução**.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="4d3cf-135">Navegue até o local onde você salvou o exemplo, clique em **WrapPST. vcproj**e, em seguida, clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="4d3cf-136">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="4d3cf-137">Na caixa de diálogo **salvar arquivo como** , clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="4d3cf-138">Na pasta onde você salvou o exemplo, clique com o botão direito do mouse no arquivo **install. bat** e, em seguida, clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="4d3cf-139">Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="4d3cf-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    

