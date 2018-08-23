---
title: Hierarquia de herança de objeto MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4b2b9971677312dbea297c9fe2d29ba65174904d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588787"
---
# <a name="mapi-object-inheritance-hierarchy"></a><span data-ttu-id="b0aa5-103">Hierarquia de herança de objeto MAPI</span><span class="sxs-lookup"><span data-stu-id="b0aa5-103">MAPI object inheritance hierarchy</span></span>

<span data-ttu-id="b0aa5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0aa5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0aa5-105">Todas as interfaces implementadas por objetos MAPI basicamente herdem [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), a interface OLE que permite a comunicação entre objetos.</span><span class="sxs-lookup"><span data-stu-id="b0aa5-105">All interfaces implemented by MAPI objects ultimately inherit from [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), the OLE interface that enables objects to communicate.</span></span> <span data-ttu-id="b0aa5-106">A maioria das interfaces herde diretamente **IUnknown**, mas algumas herdarem de uma das duas interfaces de base: [IMAPIProp: IUnknown](imapipropiunknown.md) ou [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="b0aa5-106">Most interfaces directly inherit from **IUnknown**, but some inherit from one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) or [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="b0aa5-107">A ilustração a seguir mostra a hierarquia de herança completa em MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0aa5-107">The following illustration shows the complete inheritance hierarchy in MAPI.</span></span>
  
<span data-ttu-id="b0aa5-108">**MAPI inheritance hierarchy**</span><span class="sxs-lookup"><span data-stu-id="b0aa5-108">**MAPI inheritance hierarchy**</span></span>
  
<span data-ttu-id="b0aa5-109">![Hierarquia de herança de MAPI] (media/amapi_06.gif "Hierarquia de herança de MAPI")</span><span class="sxs-lookup"><span data-stu-id="b0aa5-109">![MAPI inheritance hierarchy](media/amapi_06.gif "MAPI inheritance hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b0aa5-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0aa5-110">See also</span></span>

- [<span data-ttu-id="b0aa5-111">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0aa5-111">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md) 
- [<span data-ttu-id="b0aa5-112">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b0aa5-112">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)
- [<span data-ttu-id="b0aa5-113">Objeto MAPI e visão geral da Interface</span><span class="sxs-lookup"><span data-stu-id="b0aa5-113">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

