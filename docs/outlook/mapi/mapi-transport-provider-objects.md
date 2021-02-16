---
title: Objetos de provedor de transporte MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3f05e5b4b45e18d580737d37250e183c4cead881
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430354"
---
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="e4afd-103">Objetos de provedor de transporte MAPI</span><span class="sxs-lookup"><span data-stu-id="e4afd-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="e4afd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4afd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4afd-105">Além do provedor padrão e dos objetos de logon implementados por todos os provedores de serviços, os provedores de transporte são necessários para implementar um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="e4afd-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="e4afd-106">Para os outros tipos de provedores de serviços, implementar um objeto de status é opcional.</span><span class="sxs-lookup"><span data-stu-id="e4afd-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="e4afd-107">No entanto, o MAPI exige isso para provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="e4afd-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="e4afd-108">Os provedores de transporte que suportam o download de headers de mensagens de um servidor remoto também implementam uma pasta e uma tabela.</span><span class="sxs-lookup"><span data-stu-id="e4afd-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="e4afd-109">A ilustração a seguir mostra cada um dos objetos que os provedores de transporte podem implementar com suas interfaces correspondentes.</span><span class="sxs-lookup"><span data-stu-id="e4afd-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="e4afd-110">A ilustração também indica se MAPI ou um cliente é o usuário do objeto.</span><span class="sxs-lookup"><span data-stu-id="e4afd-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="e4afd-111">![Objetos que os provedores de transporte implementam](media/amapi_66.gif "Objetos que os provedores de transporte implementam")</span><span class="sxs-lookup"><span data-stu-id="e4afd-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e4afd-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4afd-112">See also</span></span>

- [<span data-ttu-id="e4afd-113">Objetos do provedor de serviços MAPI</span><span class="sxs-lookup"><span data-stu-id="e4afd-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)

