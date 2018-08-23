---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Modificado pela última vez: 03 de julho de 2012'
ms.openlocfilehash: 24cc4b00f02c61395565fb7ddeb6a5b5a62afdc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591937"
---
# <a name="meid"></a><span data-ttu-id="9cfe1-103">MEID</span><span class="sxs-lookup"><span data-stu-id="9cfe1-103">MEID</span></span>

 
  
<span data-ttu-id="9cfe1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cfe1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cfe1-105">Identificador de um item do Outlook.</span><span class="sxs-lookup"><span data-stu-id="9cfe1-105">Identifier for an Outlook item.</span></span> <span data-ttu-id="9cfe1-106">Ele contém um identificador de entrada e outras informações relevantes.</span><span class="sxs-lookup"><span data-stu-id="9cfe1-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9cfe1-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="9cfe1-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="9cfe1-108">Members</span><span class="sxs-lookup"><span data-stu-id="9cfe1-108">Members</span></span>

 <span data-ttu-id="9cfe1-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="9cfe1-109">_abFlags_</span></span>
  
> <span data-ttu-id="9cfe1-110">Identificador de entrada de 4 bytes do item do Outlook.</span><span class="sxs-lookup"><span data-stu-id="9cfe1-110">4-byte entry identifier for the Outlook item.</span></span> <span data-ttu-id="9cfe1-111">Para obter mais informações sobre identificadores de entrada MAPI, consulte **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="9cfe1-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="9cfe1-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="9cfe1-112">_muid_</span></span>
  
> <span data-ttu-id="9cfe1-113">GUID que identifica o provedor de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9cfe1-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="9cfe1-114">Consulte mapidefs.h para a definição de tipo de **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="9cfe1-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="9cfe1-115">_espaço reservado_</span><span class="sxs-lookup"><span data-stu-id="9cfe1-115">_placeholder_</span></span>
  
> <span data-ttu-id="9cfe1-116">Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="9cfe1-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="9cfe1-117">_ltidFld_</span><span class="sxs-lookup"><span data-stu-id="9cfe1-117">_ltidFld_</span></span>
  
> <span data-ttu-id="9cfe1-118">ID de longo prazo da pasta.</span><span class="sxs-lookup"><span data-stu-id="9cfe1-118">Long-term ID of the folder.</span></span>
    
 <span data-ttu-id="9cfe1-119">_ltidMsg_</span><span class="sxs-lookup"><span data-stu-id="9cfe1-119">_ltidMsg_</span></span>
  
> <span data-ttu-id="9cfe1-120">ID de longo prazo do item do Outlook.</span><span class="sxs-lookup"><span data-stu-id="9cfe1-120">Long-term ID of the Outlook item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9cfe1-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cfe1-121">See also</span></span>



[<span data-ttu-id="9cfe1-122">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="9cfe1-122">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9cfe1-123">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="9cfe1-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9cfe1-124">LTID</span><span class="sxs-lookup"><span data-stu-id="9cfe1-124">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="9cfe1-125">SYNC</span><span class="sxs-lookup"><span data-stu-id="9cfe1-125">SYNC</span></span>](sync.md)
  
[<span data-ttu-id="9cfe1-126">UPMSG</span><span class="sxs-lookup"><span data-stu-id="9cfe1-126">UPMSG</span></span>](upmsg.md)

