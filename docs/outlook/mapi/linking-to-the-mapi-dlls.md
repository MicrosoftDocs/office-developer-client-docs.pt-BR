---
title: Vinculando a DLLs MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0bce1d682057b81135d1684c40bc79e6710d4e2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767757"
---
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="425e7-103">Vinculando a DLLs MAPI</span><span class="sxs-lookup"><span data-stu-id="425e7-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="425e7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="425e7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="425e7-105">Clientes MAPI podem vincular a DLLs MAPI implícita ou explicitamente, usando as funções do Windows **LoadLibrary** e **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="425e7-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="425e7-106">Para obter informações sobre como vincular explicitamente DLLs MAPI, consulte o [Link para funções de MAPI](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="425e7-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="425e7-107">MAPI fornece instruções de definição de tipo no MAPIX. Arquivo de cabeçalho H para cada uma das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="425e7-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="425e7-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="425e7-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="425e7-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="425e7-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="425e7-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="425e7-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="425e7-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="425e7-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="425e7-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="425e7-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="425e7-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="425e7-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="425e7-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="425e7-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="425e7-115">Use essas definições de tipo para chamar corretamente os pontos de entrada correspondente, se você vincular explicitamente DLLs MAPI.</span><span class="sxs-lookup"><span data-stu-id="425e7-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="425e7-116">Provedores de serviços podem conter a funcionalidade de não-MAPI — recursos que estão completamente não relacionados à MAPI — em seu DLL.</span><span class="sxs-lookup"><span data-stu-id="425e7-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="425e7-117">Se você precisar usar estes recursos, chame **LoadLibrary** antes de usar a DLL e **FreeLibrary** para remover a DLL da memória depois usá-las.</span><span class="sxs-lookup"><span data-stu-id="425e7-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="425e7-118">Como MAPI está ciente dos usos de não-MAPI de um provedor de serviços DLL, não há nenhuma garantia de que a DLL esteja disponível quando necessário.</span><span class="sxs-lookup"><span data-stu-id="425e7-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="425e7-119">MAPI libera um provedor de serviços DLL quando não existem mais todos os clientes com as sessões ativas que exigem seus serviços.</span><span class="sxs-lookup"><span data-stu-id="425e7-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

