---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409808"
---
# <a name="feid"></a><span data-ttu-id="2a825-103">FEID</span><span class="sxs-lookup"><span data-stu-id="2a825-103">FEID</span></span>

 
  
<span data-ttu-id="2a825-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a825-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a825-105">Identificador de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="2a825-105">Identifier for a folder.</span></span> <span data-ttu-id="2a825-106">Ele contém um identificador de entrada e outras informações relevantes.</span><span class="sxs-lookup"><span data-stu-id="2a825-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2a825-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="2a825-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="2a825-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2a825-108">Members</span></span>

 <span data-ttu-id="2a825-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="2a825-109">_abFlags_</span></span>
  
> <span data-ttu-id="2a825-110">Identificador de entrada de 4 byte para a pasta.</span><span class="sxs-lookup"><span data-stu-id="2a825-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="2a825-111">Para obter mais informações sobre identificadores de entrada MAPI, consulte **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="2a825-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="2a825-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="2a825-112">_muid_</span></span>
  
> <span data-ttu-id="2a825-113">GUID que identifica o provedor do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2a825-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="2a825-114">Consulte mapidefs.h para a definição de tipo de **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="2a825-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="2a825-115">_espaço reservado_</span><span class="sxs-lookup"><span data-stu-id="2a825-115">_placeholder_</span></span>
  
> <span data-ttu-id="2a825-116">Este membro está reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="2a825-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="2a825-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="2a825-117">_ltid_</span></span>
  
> <span data-ttu-id="2a825-118">ID de longo prazo da pasta.</span><span class="sxs-lookup"><span data-stu-id="2a825-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a825-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a825-119">See also</span></span>



[<span data-ttu-id="2a825-120">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="2a825-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2a825-121">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="2a825-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2a825-122">LTID</span><span class="sxs-lookup"><span data-stu-id="2a825-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="2a825-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="2a825-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="2a825-124">SYNC</span><span class="sxs-lookup"><span data-stu-id="2a825-124">SYNC</span></span>](sync.md)

