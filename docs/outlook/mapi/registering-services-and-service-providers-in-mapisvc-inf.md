---
title: Registrando provedores de serviços e serviços no MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Última modificação: 18 de julho de 2013'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328368"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a><span data-ttu-id="170c5-103">Registrando provedores de serviços e serviços no MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="170c5-103">Registering Services and Service Providers in MapiSvc.inf</span></span>

 
  
<span data-ttu-id="170c5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="170c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="170c5-105">A instalação de um novo provedor em um sistema requer a atualização do arquivo MapiSvc.inf para apontar para o novo provedor.</span><span class="sxs-lookup"><span data-stu-id="170c5-105">Installing a new provider on a system requires updating the MapiSvc.inf file to point to the new provider.</span></span> <span data-ttu-id="170c5-106">Propriedades padrão definidas durante a configuração, que incluem o seguinte, informam ao MAPI onde encontrar a biblioteca de vínculo dinâmico do provedor (.dll):</span><span class="sxs-lookup"><span data-stu-id="170c5-106">Standard properties set during configuration, which include the following, inform MAPI where to find the provider's dynamic-link library (.dll):</span></span>
  
- <span data-ttu-id="170c5-107">A **PR_SERVICE_DLL_NAME** é especificada na **seção [Serviço de** Mensagens].</span><span class="sxs-lookup"><span data-stu-id="170c5-107">The **PR_SERVICE_DLL_NAME** is specified in the **[Message Service]** section.</span></span> 
    
- <span data-ttu-id="170c5-108">O **PR_PROVIDER_DLL_NAME** especificado na seção **[Provedor de** Serviços].</span><span class="sxs-lookup"><span data-stu-id="170c5-108">The **PR_PROVIDER_DLL_NAME** is specified in the **[Service Provider]** section.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="170c5-109">A expectativa é que você de definir o nome da .dll do provedor (sem o sufixo "32").</span><span class="sxs-lookup"><span data-stu-id="170c5-109">The expectation is that you set the name of your provider's .dll (without the suffix "32").</span></span> <span data-ttu-id="170c5-110">MAPI then loads your provider by looking for it on the path.</span><span class="sxs-lookup"><span data-stu-id="170c5-110">MAPI then loads your provider by looking for it on the path.</span></span> 
  
## <a name="putting-a-path-in-mapisvcinf"></a><span data-ttu-id="170c5-111">Colocando um caminho em MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="170c5-111">Putting a Path in MapiSvc.inf</span></span>

<span data-ttu-id="170c5-112">A maioria dos aplicativos é instalada em Arquivos de Programas, exigindo uma atualização na variável de caminho para permitir que provedores MAPI funcionem.</span><span class="sxs-lookup"><span data-stu-id="170c5-112">Most applications install under Program Files, requiring an update to the path variable to allow MAPI providers to work.</span></span> <span data-ttu-id="170c5-113">Com algumas restrições, o Microsoft Outlook 2010 e o Outlook 2013 podem acomodar caminhos completos para provedores mapi.</span><span class="sxs-lookup"><span data-stu-id="170c5-113">With a few restrictions Microsoft Outlook 2010 and Outlook 2013 can accommodate full paths to MAPI providers.</span></span>
  
<span data-ttu-id="170c5-114">Ao registrar seu provedor em MapiSvc.inf, você pode colocar o caminho completo para o provedor nas propriedades MAPI **PR_SERVICE_DLL_NAME** e **PR_PROVIDER_DLL_NAME**.</span><span class="sxs-lookup"><span data-stu-id="170c5-114">When registering your provider in MapiSvc.inf, you could put the full path to the provider in the MAPI properties **PR_SERVICE_DLL_NAME** and **PR_PROVIDER_DLL_NAME**.</span></span>
  
<span data-ttu-id="170c5-115">Em qualquer uma das propriedades, o caminho completo deve estar sem o sufixo "32", pois o MAPI continua anexando-o ao nome do arquivo antes de procurar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="170c5-115">In either property, the full path must be without the suffix "32", because MAPI continues to append that to the filename before looking for your file.</span></span> <span data-ttu-id="170c5-116">Isso significa que, se você registrar o caminho "c:\mypath\myprovider.dll", o MAPI tentará carregar "c:\mypath\myprovider32.dll".</span><span class="sxs-lookup"><span data-stu-id="170c5-116">This means that if you register the path "c:\mypath\myprovider.dll", MAPI will attempt to load "c:\mypath\myprovider32.dll".</span></span>
  
<span data-ttu-id="170c5-117">Como o MAPI do Outlook não foi originalmente projetado para acomodar caminhos completos, ele realiza essa inserção do sufixo "32" procurando pelo primeiro período na cadeia de caracteres, o que significa que caminhos que contêm outros períodos não podem funcionar, portanto, você não pode usar caminhos como "c:\my.path\myprovider.dll" ou "c:\mypath\my.provider.dll".</span><span class="sxs-lookup"><span data-stu-id="170c5-117">Because Outlook's MAPI was not originally designed to accommodate full paths, it accomplishes this insertion of the "32" suffix by looking for the first period in the string, which means that paths that contain other periods cannot work, so you cannot use paths such as "c:\my.path\myprovider.dll" or "c:\mypath\my.provider.dll".</span></span>
  
<span data-ttu-id="170c5-118">Às vezes, em um provedor de repositório, você gera identificadores de entrada usando a **função WrapStoreEntryID,** que usa como parâmetro o nome do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="170c5-118">Sometimes in a store provider you will generate entry identifiers using the **WrapStoreEntryID** function, which takes as a parameter the name of your provider.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="170c5-119">Se você estiver usando caminhos completos em MapiSvc.inf, deverá usar o mesmo caminho em qualquer chamada para **WrapStoreEntryID**.</span><span class="sxs-lookup"><span data-stu-id="170c5-119">If you are using full paths in MapiSvc.inf, you must use the same path in any calls to **WrapStoreEntryID**.</span></span> 
  
<span data-ttu-id="170c5-120">Além disso, o caminho usado pode ser convertido de e para Unicode usando a página de código fornecida pela [função GetACP.](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/)</span><span class="sxs-lookup"><span data-stu-id="170c5-120">Additionally, the path you use may be converted to and from Unicode using the code page provided by the [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) function.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="170c5-121">Haverá falha se você escolher um caminho que contenha caracteres que não podem sobreviver a tal ida e volta por meio das funções [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) e [WideCharToMultiByte.](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/)</span><span class="sxs-lookup"><span data-stu-id="170c5-121">You will experience failure if you choose a path that contains characters that cannot survive such a roundtrip through the [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) and [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) functions.</span></span> 
  
<span data-ttu-id="170c5-122">Para uma demonstração dessa funcionalidade, o exemplo [PST](https://github.com/stephenegriffin/Outlook2010CodeSamples) empacotado no GitHub foi revisado - a funcionalidade pertinente está em **MergeWithMapiSvc** e **GenerateProviderPath**.</span><span class="sxs-lookup"><span data-stu-id="170c5-122">For a demonstration of this functionality, the [Wrapped PST sample](https://github.com/stephenegriffin/Outlook2010CodeSamples) on GitHub has been revised - the pertinent functionality is in **MergeWithMapiSvc** and **GenerateProviderPath**.</span></span>
  

