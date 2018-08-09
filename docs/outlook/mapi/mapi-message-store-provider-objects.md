---
title: Objetos de provedor de armazenamento de mensagem MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 87a452e6-dedf-414d-b7cf-07c8b02dd94a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f5bdf4a4cbf67aa9524819ffe4eee14b62714632
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767888"
---
# <a name="mapi-message-store-provider-objects"></a><span data-ttu-id="a336d-103">Objetos de provedor de armazenamento de mensagem MAPI</span><span class="sxs-lookup"><span data-stu-id="a336d-103">MAPI message store provider objects</span></span>
  
<span data-ttu-id="a336d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a336d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a336d-105">Provedores de armazenamento de mensagem implementam provedor e objetos de logon, como todos os provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="a336d-105">Message store providers implement provider and logon objects, as do all service providers.</span></span> <span data-ttu-id="a336d-106">Eles também implementam um objeto de repositório de mensagem, pastas, mensagens, anexos e tabelas.</span><span class="sxs-lookup"><span data-stu-id="a336d-106">They also implement a message store object, folders, messages, attachments, and tables.</span></span> <span data-ttu-id="a336d-107">Como opção, alguns provedores de armazenamento de mensagem implementam objetos de status.</span><span class="sxs-lookup"><span data-stu-id="a336d-107">As an option, some message store providers implement status objects.</span></span>
  
<span data-ttu-id="a336d-108">A ilustração a seguir mostra cada objeto de repositório de mensagem com sua interface correspondente e o componente MAPI que a utilizam.</span><span class="sxs-lookup"><span data-stu-id="a336d-108">The following illustration shows each message store object with its corresponding interface and the MAPI component that uses it.</span></span>
  
<span data-ttu-id="a336d-109">![Objetos que implementam provedores de armazenamento de mensagem] (media/amapi_63.gif "Objetos que implementam provedores de armazenamento de mensagem")</span><span class="sxs-lookup"><span data-stu-id="a336d-109">![Objects that message store providers implement](media/amapi_63.gif "Objects that message store providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a336d-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="a336d-110">See also</span></span>

- [<span data-ttu-id="a336d-111">Objetos do provedor de serviço MAPI</span><span class="sxs-lookup"><span data-stu-id="a336d-111">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)

