---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f4ece0662b72047b785b03f3134c96fac48c219a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770436"
---
# <a name="skey"></a><span data-ttu-id="d606f-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="d606f-103">SKEY</span></span>

  
  
<span data-ttu-id="d606f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d606f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d606f-105">Chave de origem para um item do Outlook.</span><span class="sxs-lookup"><span data-stu-id="d606f-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d606f-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d606f-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="d606f-107">Members</span><span class="sxs-lookup"><span data-stu-id="d606f-107">Members</span></span>

 <span data-ttu-id="d606f-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="d606f-108">_guid_</span></span>
  
> <span data-ttu-id="d606f-109">GUID do servidor criando o objeto.</span><span class="sxs-lookup"><span data-stu-id="d606f-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d606f-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="d606f-110">See also</span></span>



[<span data-ttu-id="d606f-111">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="d606f-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="d606f-112">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="d606f-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="d606f-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="d606f-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="d606f-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="d606f-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="d606f-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="d606f-115">UPREADE</span></span>](upreade.md)
