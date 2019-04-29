---
title: Vincular a DLLs MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 394537a60f4cb9603024115ccea67570291d8ac6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419300"
---
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="3e43e-103">Vincular a DLLs MAPI</span><span class="sxs-lookup"><span data-stu-id="3e43e-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="3e43e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e43e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e43e-105">Os clientes MAPI podem vincular as DLLs MAPI implicitamente ou explicitamente usando as funções do Windows **LoadLibrary** e **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="3e43e-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="3e43e-106">Para obter informações sobre como vincular DLLs MAPI explicitamente, consulte [link to MAPI Functions](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="3e43e-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="3e43e-107">MAPI fornece instruções de definição de tipo no MAPIX. Arquivo de cabeçalho H para cada uma das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="3e43e-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="3e43e-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="3e43e-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="3e43e-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="3e43e-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="3e43e-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="3e43e-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="3e43e-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="3e43e-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="3e43e-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="3e43e-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="3e43e-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3e43e-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3e43e-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="3e43e-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="3e43e-115">Use essas definições de tipo para chamar corretamente os pontos de entrada correspondentes se você vincular explicitamente às DLLs MAPI.</span><span class="sxs-lookup"><span data-stu-id="3e43e-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="3e43e-116">Os provedores de serviços podem conter funcionalidade não MAPI, recursos que não são completamente relacionados ao MAPI — em sua DLL.</span><span class="sxs-lookup"><span data-stu-id="3e43e-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="3e43e-117">Se você precisar usar esses recursos, chame **LoadLibrary** antes de usar a dll e o **FreeLibrary** para remover a DLL da memória após o uso.</span><span class="sxs-lookup"><span data-stu-id="3e43e-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="3e43e-118">Como o MAPI não está ciente de usos não MAPI de uma DLL de provedor de serviços, não há garantia de que a DLL estará disponível quando necessário.</span><span class="sxs-lookup"><span data-stu-id="3e43e-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="3e43e-119">O MAPI libera uma DLL de provedor de serviços quando não há mais clientes com sessões ativas que exigem seus serviços.</span><span class="sxs-lookup"><span data-stu-id="3e43e-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

