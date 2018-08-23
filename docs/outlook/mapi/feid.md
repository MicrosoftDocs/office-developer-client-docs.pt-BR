---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Modificado pela última vez: 02 de julho de 2012'
ms.openlocfilehash: 3e534f91863e2a1300e03d112d1f532f486eedd9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588304"
---
# <a name="feid"></a><span data-ttu-id="702f8-103">FEID</span><span class="sxs-lookup"><span data-stu-id="702f8-103">FEID</span></span>

 
  
<span data-ttu-id="702f8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="702f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="702f8-105">Identificador de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="702f8-105">Identifier for a folder.</span></span> <span data-ttu-id="702f8-106">Ele contém um identificador de entrada e outras informações relevantes.</span><span class="sxs-lookup"><span data-stu-id="702f8-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="702f8-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="702f8-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="702f8-108">Members</span><span class="sxs-lookup"><span data-stu-id="702f8-108">Members</span></span>

 <span data-ttu-id="702f8-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="702f8-109">_abFlags_</span></span>
  
> <span data-ttu-id="702f8-110">Identificador de entrada de 4 bytes para a pasta.</span><span class="sxs-lookup"><span data-stu-id="702f8-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="702f8-111">Para obter mais informações sobre identificadores de entrada MAPI, consulte **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="702f8-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="702f8-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="702f8-112">_muid_</span></span>
  
> <span data-ttu-id="702f8-113">GUID que identifica o provedor de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="702f8-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="702f8-114">Consulte mapidefs.h para a definição de tipo de **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="702f8-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="702f8-115">_espaço reservado_</span><span class="sxs-lookup"><span data-stu-id="702f8-115">_placeholder_</span></span>
  
> <span data-ttu-id="702f8-116">Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="702f8-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="702f8-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="702f8-117">_ltid_</span></span>
  
> <span data-ttu-id="702f8-118">ID de longo prazo da pasta.</span><span class="sxs-lookup"><span data-stu-id="702f8-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="702f8-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="702f8-119">See also</span></span>



[<span data-ttu-id="702f8-120">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="702f8-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="702f8-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="702f8-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="702f8-122">LTID</span><span class="sxs-lookup"><span data-stu-id="702f8-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="702f8-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="702f8-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="702f8-124">SYNC</span><span class="sxs-lookup"><span data-stu-id="702f8-124">SYNC</span></span>](sync.md)

