---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 26b08535d81cb961ed0ace70ea227316b30cd526
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573457"
---
# <a name="skey"></a><span data-ttu-id="89fd4-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="89fd4-103">SKEY</span></span>

  
  
<span data-ttu-id="89fd4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89fd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89fd4-105">Chave de origem para um item do Outlook.</span><span class="sxs-lookup"><span data-stu-id="89fd4-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="89fd4-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="89fd4-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="89fd4-107">Members</span><span class="sxs-lookup"><span data-stu-id="89fd4-107">Members</span></span>

 <span data-ttu-id="89fd4-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="89fd4-108">_guid_</span></span>
  
> <span data-ttu-id="89fd4-109">GUID do servidor criando o objeto.</span><span class="sxs-lookup"><span data-stu-id="89fd4-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="89fd4-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="89fd4-110">See also</span></span>



[<span data-ttu-id="89fd4-111">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="89fd4-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="89fd4-112">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="89fd4-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="89fd4-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="89fd4-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="89fd4-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="89fd4-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="89fd4-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="89fd4-115">UPREADE</span></span>](upreade.md)

