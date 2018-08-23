---
title: Registrar provedores de serviços e serviços no MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Modificado pela última vez: 18 de julho de 2013'
ms.openlocfilehash: c74257b84636952b26c5a624f4f7f76f66be9149
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566919"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a><span data-ttu-id="c2e8a-103">Registrar provedores de serviços e serviços no MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="c2e8a-103">Registering Services and Service Providers in MapiSvc.inf</span></span>

 
  
<span data-ttu-id="c2e8a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2e8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2e8a-105">A instalação de um novo provedor em um sistema requer atualizando o arquivo Mapisvc para apontar para o novo provedor.</span><span class="sxs-lookup"><span data-stu-id="c2e8a-105">Installing a new provider on a system requires updating the MapiSvc.inf file to point to the new provider.</span></span> <span data-ttu-id="c2e8a-106">Propriedades padrão definida durante a configuração, que incluem o seguinte, informam MAPI onde encontrar a biblioteca de vínculo dinâmico do provedor (. dll):</span><span class="sxs-lookup"><span data-stu-id="c2e8a-106">Standard properties set during configuration, which include the following, inform MAPI where to find the provider's dynamic-link library (.dll):</span></span>
  
- <span data-ttu-id="c2e8a-107">O **PR_SERVICE_DLL_NAME** é especificado na seção **[Serviço de mensagem]** .</span><span class="sxs-lookup"><span data-stu-id="c2e8a-107">The **PR_SERVICE_DLL_NAME** is specified in the **[Message Service]** section.</span></span> 
    
- <span data-ttu-id="c2e8a-108">O **PR_PROVIDER_DLL_NAME** é especificado na seção **[Serviço provedor]** .</span><span class="sxs-lookup"><span data-stu-id="c2e8a-108">The **PR_PROVIDER_DLL_NAME** is specified in the **[Service Provider]** section.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="c2e8a-109">A expectativa é que você defina o nome do. dll do seu provedor (sem o sufixo "32").</span><span class="sxs-lookup"><span data-stu-id="c2e8a-109">The expectation is that you set the name of your provider's .dll (without the suffix "32").</span></span> <span data-ttu-id="c2e8a-110">MAPI então carrega o seu provedor procurando por ela no caminho.</span><span class="sxs-lookup"><span data-stu-id="c2e8a-110">MAPI then loads your provider by looking for it on the path.</span></span> 
  
## <a name="putting-a-path-in-mapisvcinf"></a><span data-ttu-id="c2e8a-111">Colocar um caminho em MAPISVC</span><span class="sxs-lookup"><span data-stu-id="c2e8a-111">Putting a Path in MapiSvc.inf</span></span>

<span data-ttu-id="c2e8a-112">A maioria dos aplicativos são instalados em arquivos de programas que requerem uma atualização para a variável path para permitir que os provedores MAPI trabalhar.</span><span class="sxs-lookup"><span data-stu-id="c2e8a-112">Most applications install under Program Files, requiring an update to the path variable to allow MAPI providers to work.</span></span> <span data-ttu-id="c2e8a-113">Com algumas restrições Microsoft Outlook 2010 e o Outlook 2013 podem acomodar caminhos completos para provedores MAPI.</span><span class="sxs-lookup"><span data-stu-id="c2e8a-113">With a few restrictions Microsoft Outlook 2010 and Outlook 2013 can accommodate full paths to MAPI providers.</span></span>
  
<span data-ttu-id="c2e8a-114">Ao registrar seu provedor no Mapisvc, você poderia colocar o caminho completo para o provedor nas propriedades do MAPI **PR_SERVICE_DLL_NAME** e **PR_PROVIDER_DLL_NAME**.</span><span class="sxs-lookup"><span data-stu-id="c2e8a-114">When registering your provider in MapiSvc.inf, you could put the full path to the provider in the MAPI properties **PR_SERVICE_DLL_NAME** and **PR_PROVIDER_DLL_NAME**.</span></span>
  
<span data-ttu-id="c2e8a-115">Em ambas as propriedades o caminho completo deve estar sem o sufixo "32", porque MAPI continua a acrescente que o nome do arquivo antes procurando o arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2e8a-115">In either property, the full path must be without the suffix "32", because MAPI continues to append that to the filename before looking for your file.</span></span> <span data-ttu-id="c2e8a-116">Isso significa que se registrar o caminho "c:\mypath\myprovider.dll", MAPI tentará carregar "c:\mypath\myprovider32.dll".</span><span class="sxs-lookup"><span data-stu-id="c2e8a-116">This means that if you register the path "c:\mypath\myprovider.dll", MAPI will attempt to load "c:\mypath\myprovider32.dll".</span></span>
  
<span data-ttu-id="c2e8a-117">Porque do Outlook MAPI não foi originalmente criado para acomodar os caminhos completos, ele realiza a inserção do sufixo "32" observando para o primeiro período na cadeia de caracteres, o que significa que os caminhos que contêm outros períodos não podem funcionar, portanto, você não pode usar caminhos como "c:\my.path\myprovider.dll" ou "c:\mypath\my.provider.dll".</span><span class="sxs-lookup"><span data-stu-id="c2e8a-117">Because Outlook's MAPI was not originally designed to accommodate full paths, it accomplishes this insertion of the "32" suffix by looking for the first period in the string, which means that paths that contain other periods cannot work, so you cannot use paths such as "c:\my.path\myprovider.dll" or "c:\mypath\my.provider.dll".</span></span>
  
<span data-ttu-id="c2e8a-118">Em alguns casos, em um provedor de armazenamento você irá gerar identificadores de entrada usando a função **WrapStoreEntryID** , que tem como um parâmetro, o nome do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="c2e8a-118">Sometimes in a store provider you will generate entry identifiers using the **WrapStoreEntryID** function, which takes as a parameter the name of your provider.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="c2e8a-119">Se você estiver usando caminhos completos em MAPISVC, você deve usar o mesmo caminho em todas as chamadas para **WrapStoreEntryID**.</span><span class="sxs-lookup"><span data-stu-id="c2e8a-119">If you are using full paths in MapiSvc.inf, you must use the same path in any calls to **WrapStoreEntryID**.</span></span> 
  
<span data-ttu-id="c2e8a-120">Além disso, o caminho que você usar pode ser convertido em Unicode usando a página de código fornecida pela função [GetACP](http://msdn.microsoft.com/en-us/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) .</span><span class="sxs-lookup"><span data-stu-id="c2e8a-120">Additionally, the path you use may be converted to and from Unicode using the code page provided by the [GetACP](http://msdn.microsoft.com/en-us/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) function.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="c2e8a-121">Fica falha se você escolher um caminho que contém caracteres que não podem sobreviver tal uma ida e volta por meio das funções [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) e [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) .</span><span class="sxs-lookup"><span data-stu-id="c2e8a-121">You will experience failure if you choose a path that contains characters that cannot survive such a roundtrip through the [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) and [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) functions.</span></span> 
  
<span data-ttu-id="c2e8a-122">Para obter uma demonstração dessa funcionalidade, a [amostra de PST quebrado automaticamente](http://ol2010mapisamples.codeplex.com/) no CodePlex foi revisado - a funcionalidade pertinente está em **MergeWithMapiSvc** e **GenerateProviderPath**.</span><span class="sxs-lookup"><span data-stu-id="c2e8a-122">For a demonstration of this functionality, the [Wrapped PST sample](http://ol2010mapisamples.codeplex.com/) on CodePlex has been revised - the pertinent functionality is in **MergeWithMapiSvc** and **GenerateProviderPath**.</span></span>
  

