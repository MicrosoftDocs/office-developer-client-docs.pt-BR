---
title: Objetos do provedor de transporte MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2d7311857ff54ef253fd00634671f4a510443f19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767968"
---
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="58177-103">Objetos do provedor de transporte MAPI</span><span class="sxs-lookup"><span data-stu-id="58177-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="58177-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58177-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58177-105">Além do provedor padrão e objetos de logon implementados por todos os provedores de serviços, provedores de transporte são necessários para implementar um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="58177-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="58177-106">Para os outros tipos de provedor de serviço, a implementação de um objeto de status é opcional.</span><span class="sxs-lookup"><span data-stu-id="58177-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="58177-107">No entanto, MAPI exige que ele para provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="58177-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="58177-108">Provedores de transporte que suportam o download de cabeçalhos de mensagem de um servidor remoto também implementam uma pasta e uma tabela.</span><span class="sxs-lookup"><span data-stu-id="58177-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="58177-109">A ilustração a seguir mostra cada um dos objetos que podem ser implementar provedores de transporte com suas interfaces correspondentes.</span><span class="sxs-lookup"><span data-stu-id="58177-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="58177-110">A ilustração também indica se MAPI ou um cliente é o usuário do objeto.</span><span class="sxs-lookup"><span data-stu-id="58177-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="58177-111">![Objetos que implementam provedores de transporte] (media/amapi_66.gif "Objetos que implementam provedores de transporte")</span><span class="sxs-lookup"><span data-stu-id="58177-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="58177-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="58177-112">See also</span></span>

- [<span data-ttu-id="58177-113">Objetos do provedor de serviço MAPI</span><span class="sxs-lookup"><span data-stu-id="58177-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)

