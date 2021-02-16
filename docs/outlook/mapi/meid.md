---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: a9aea0db700de9c82aa2a41a443ebf03da8ce9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430305"
---
# <a name="meid"></a><span data-ttu-id="70773-103">MEID</span><span class="sxs-lookup"><span data-stu-id="70773-103">MEID</span></span>

 
  
<span data-ttu-id="70773-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70773-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70773-105">Identificador de um item do Outlook.</span><span class="sxs-lookup"><span data-stu-id="70773-105">Identifier for an Outlook item.</span></span> <span data-ttu-id="70773-106">Ele contém um identificador de entrada e outras informações relevantes.</span><span class="sxs-lookup"><span data-stu-id="70773-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="70773-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="70773-107">Quick info</span></span>

```cpp
struct MEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltidFld; 
    LTID ltidMsg; 
};
```

## <a name="members"></a><span data-ttu-id="70773-108">Membros</span><span class="sxs-lookup"><span data-stu-id="70773-108">Members</span></span>

 <span data-ttu-id="70773-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="70773-109">_abFlags_</span></span>
  
> <span data-ttu-id="70773-110">Identificador de entrada de 4 byte para o item do Outlook.</span><span class="sxs-lookup"><span data-stu-id="70773-110">4-byte entry identifier for the Outlook item.</span></span> <span data-ttu-id="70773-111">Para obter mais informações sobre identificadores de entrada MAPI, consulte **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="70773-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="70773-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="70773-112">_muid_</span></span>
  
> <span data-ttu-id="70773-113">GUID que identifica o provedor do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="70773-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="70773-114">Consulte mapidefs.h para a definição de tipo de **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="70773-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="70773-115">_espaço reservado_</span><span class="sxs-lookup"><span data-stu-id="70773-115">_placeholder_</span></span>
  
> <span data-ttu-id="70773-116">Este membro está reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="70773-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="70773-117">_ltidFld_</span><span class="sxs-lookup"><span data-stu-id="70773-117">_ltidFld_</span></span>
  
> <span data-ttu-id="70773-118">ID de longo prazo da pasta.</span><span class="sxs-lookup"><span data-stu-id="70773-118">Long-term ID of the folder.</span></span>
    
 <span data-ttu-id="70773-119">_ltidMsg_</span><span class="sxs-lookup"><span data-stu-id="70773-119">_ltidMsg_</span></span>
  
> <span data-ttu-id="70773-120">ID de longo prazo do item do Outlook.</span><span class="sxs-lookup"><span data-stu-id="70773-120">Long-term ID of the Outlook item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70773-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="70773-121">See also</span></span>



[<span data-ttu-id="70773-122">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="70773-122">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="70773-123">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="70773-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="70773-124">LTID</span><span class="sxs-lookup"><span data-stu-id="70773-124">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="70773-125">SYNC</span><span class="sxs-lookup"><span data-stu-id="70773-125">SYNC</span></span>](sync.md)
  
[<span data-ttu-id="70773-126">UPMSG</span><span class="sxs-lookup"><span data-stu-id="70773-126">UPMSG</span></span>](upmsg.md)

