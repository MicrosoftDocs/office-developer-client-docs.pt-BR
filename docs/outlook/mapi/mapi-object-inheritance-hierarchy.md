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
ms.openlocfilehash: a03b994a613bbb1f17db3e3220b7e053989c278a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767890"
---
# <a name="mapi-object-inheritance-hierarchy"></a><span data-ttu-id="b6f5b-103">Hierarquia de herança de objeto MAPI</span><span class="sxs-lookup"><span data-stu-id="b6f5b-103">MAPI object inheritance hierarchy</span></span>

<span data-ttu-id="b6f5b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6f5b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6f5b-105">Todas as interfaces implementadas por objetos MAPI basicamente herdem [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), a interface OLE que permite a comunicação entre objetos.</span><span class="sxs-lookup"><span data-stu-id="b6f5b-105">All interfaces implemented by MAPI objects ultimately inherit from [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), the OLE interface that enables objects to communicate.</span></span> <span data-ttu-id="b6f5b-106">A maioria das interfaces herde diretamente **IUnknown**, mas algumas herdarem de uma das duas interfaces de base: [IMAPIProp: IUnknown](imapipropiunknown.md) ou [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="b6f5b-106">Most interfaces directly inherit from **IUnknown**, but some inherit from one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) or [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="b6f5b-107">A ilustração a seguir mostra a hierarquia de herança completa em MAPI.</span><span class="sxs-lookup"><span data-stu-id="b6f5b-107">The following illustration shows the complete inheritance hierarchy in MAPI.</span></span>
  
<span data-ttu-id="b6f5b-108">**MAPI inheritance hierarchy**</span><span class="sxs-lookup"><span data-stu-id="b6f5b-108">**MAPI inheritance hierarchy**</span></span>
  
<span data-ttu-id="b6f5b-109">![Hierarquia de herança de MAPI] (media/amapi_06.gif "Hierarquia de herança de MAPI")</span><span class="sxs-lookup"><span data-stu-id="b6f5b-109">![MAPI inheritance hierarchy](media/amapi_06.gif "MAPI inheritance hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b6f5b-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6f5b-110">See also</span></span>

- [<span data-ttu-id="b6f5b-111">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6f5b-111">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md) 
- [<span data-ttu-id="b6f5b-112">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b6f5b-112">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)
- [<span data-ttu-id="b6f5b-113">Objeto MAPI e visão geral da Interface</span><span class="sxs-lookup"><span data-stu-id="b6f5b-113">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

