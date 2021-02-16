---
title: Exemplo de provedor de armazenamento de mensagens
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
# <a name="message-store-provider-sample"></a><span data-ttu-id="ddfff-103">Exemplo de provedor de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="ddfff-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="ddfff-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddfff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddfff-105">O Provedor de Armazenamento PST com Conteúdo de Exemplo usa um provedor de arquivos de Pastas Particulares (PST) como back-end para armazenar dados.</span><span class="sxs-lookup"><span data-stu-id="ddfff-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="ddfff-106">O provedor de armazenamento PST empacotado deve ser usado junto com a API de Replicação.</span><span class="sxs-lookup"><span data-stu-id="ddfff-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="ddfff-107">A API de Replicação permite replicar itens de um repositório de dados back-end para um repositório PST do Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="ddfff-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="ddfff-108">Use a API de Replicação para replicar os dados em um armazenamento PST dedicado e acompanhar o estado de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ddfff-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="ddfff-109">Para obter mais informações, consulte [Sobre a API de replicação.](about-the-replication-api.md)</span><span class="sxs-lookup"><span data-stu-id="ddfff-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="ddfff-110">A maioria das funções no Provedor de Armazenamento PST com Fim de Exemplo passa seus argumentos diretamente para o provedor de PST subjacente.</span><span class="sxs-lookup"><span data-stu-id="ddfff-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="ddfff-111">Determinadas funções exigem implementação especial e são descritas nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ddfff-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ddfff-112">Executável:</span><span class="sxs-lookup"><span data-stu-id="ddfff-112">Executable:</span></span>  <br/> |<span data-ttu-id="ddfff-113">WrpPST32.dll</span><span class="sxs-lookup"><span data-stu-id="ddfff-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="ddfff-114">Diretório do código-fonte:</span><span class="sxs-lookup"><span data-stu-id="ddfff-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="ddfff-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="ddfff-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="ddfff-116">Idioma:</span><span class="sxs-lookup"><span data-stu-id="ddfff-116">Language:</span></span>  <br/> |<span data-ttu-id="ddfff-117">C++</span><span class="sxs-lookup"><span data-stu-id="ddfff-117">C++</span></span>  <br/> |
|<span data-ttu-id="ddfff-118">Plataformas:</span><span class="sxs-lookup"><span data-stu-id="ddfff-118">Platforms:</span></span>  <br/> |<span data-ttu-id="ddfff-119">Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="ddfff-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="ddfff-120">Recursos com suporte</span><span class="sxs-lookup"><span data-stu-id="ddfff-120">Supported Features</span></span>

<span data-ttu-id="ddfff-121">Este exemplo dá suporte ao Microsoft Outlook 2010 de 64 bits e agora foi revisado para o Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="ddfff-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="ddfff-122">Consulte os tópicos a seguir para obter informações adicionais:</span><span class="sxs-lookup"><span data-stu-id="ddfff-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="ddfff-123">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="ddfff-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="ddfff-124">Inicializando um provedor de armazenamento PST empacotado</span><span class="sxs-lookup"><span data-stu-id="ddfff-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="ddfff-125">Logondo em um provedor de armazenamento PST empacotado</span><span class="sxs-lookup"><span data-stu-id="ddfff-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="ddfff-126">Usando um provedor de armazenamento PST empacotado</span><span class="sxs-lookup"><span data-stu-id="ddfff-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="ddfff-127">Desligar um provedor de armazenamento PST empacotado</span><span class="sxs-lookup"><span data-stu-id="ddfff-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="ddfff-128">**Para instalar o Sample Wrapped PST Store Provider**</span><span class="sxs-lookup"><span data-stu-id="ddfff-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="ddfff-129">Para baixar o Exemplo de Provedor de PST com Fim, consulte [Baixando os exemplos de MAPI do Outlook.](downloading-the-outlook-mapi-samples.md)</span><span class="sxs-lookup"><span data-stu-id="ddfff-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="ddfff-130">Localize a pasta onde você salvou os exemplos de MAPI do Outlook.</span><span class="sxs-lookup"><span data-stu-id="ddfff-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="ddfff-131">Clique com o botão direito do mouse na pasta zip do número de versão do **OutlookMAPISamples \< \>** e clique em **Extrair Tudo.**</span><span class="sxs-lookup"><span data-stu-id="ddfff-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="ddfff-132">Clique **em** Procurar, selecione o local onde deseja salvar o exemplo e clique em **Extrair.**</span><span class="sxs-lookup"><span data-stu-id="ddfff-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="ddfff-133">Execute o Microsoft Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="ddfff-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="ddfff-134">No Microsoft Visual Studio 2008, clique em **Arquivo,** selecione **Abrir** e clique em **Projeto/Solução.**</span><span class="sxs-lookup"><span data-stu-id="ddfff-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="ddfff-135">Navegue até o local onde você salvou o exemplo, clique em **WrapPST.vcproj** e clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="ddfff-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="ddfff-136">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="ddfff-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="ddfff-137">Na caixa **de diálogo Salvar Arquivo como,** clique em **Salvar.**</span><span class="sxs-lookup"><span data-stu-id="ddfff-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="ddfff-138">Na pasta onde você salvou o exemplo, clique com o botão direito do mouse no arquivo **install.bat** e clique em **Executar como administrador.**</span><span class="sxs-lookup"><span data-stu-id="ddfff-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="ddfff-139">Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="ddfff-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    

