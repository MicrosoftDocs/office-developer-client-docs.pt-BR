---
title: Hierarquia de herança de objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4b610415089ff19165ffcabc9e13901ed63c907d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345834"
---
# <a name="mapi-object-inheritance-hierarchy"></a><span data-ttu-id="fe619-103">Hierarquia de herança de objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="fe619-103">MAPI object inheritance hierarchy</span></span>

<span data-ttu-id="fe619-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe619-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe619-105">Todas as interfaces implementadas por objetos MAPI herdam, em última análise, [de IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), a interface OLE que permite que os objetos se comuniquem.</span><span class="sxs-lookup"><span data-stu-id="fe619-105">All interfaces implemented by MAPI objects ultimately inherit from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), the OLE interface that enables objects to communicate.</span></span> <span data-ttu-id="fe619-106">A maioria das interfaces herda diretamente de **IUnknown**, mas algumas herdam de uma de duas outras interfaces base: [IMAPIProp : IUnknown](imapipropiunknown.md) ou [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="fe619-106">Most interfaces directly inherit from **IUnknown**, but some inherit from one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) or [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="fe619-107">A ilustração a seguir mostra a hierarquia de herança completa em MAPI.</span><span class="sxs-lookup"><span data-stu-id="fe619-107">The following illustration shows the complete inheritance hierarchy in MAPI.</span></span>
  
<span data-ttu-id="fe619-108">**MAPI inheritance hierarchy**</span><span class="sxs-lookup"><span data-stu-id="fe619-108">**MAPI inheritance hierarchy**</span></span>
  
<span data-ttu-id="fe619-109">![Hierarquia de herança MAPI da](media/amapi_06.gif "hierarquia de herança MAPI")</span><span class="sxs-lookup"><span data-stu-id="fe619-109">![MAPI inheritance hierarchy](media/amapi_06.gif "MAPI inheritance hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fe619-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe619-110">See also</span></span>

- [<span data-ttu-id="fe619-111">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fe619-111">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md) 
- [<span data-ttu-id="fe619-112">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fe619-112">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)
- [<span data-ttu-id="fe619-113">Visão geral de objetos e interface MAPI</span><span class="sxs-lookup"><span data-stu-id="fe619-113">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

