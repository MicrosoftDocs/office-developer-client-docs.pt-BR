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
ms.openlocfilehash: bb2d347d218a7c33a2184bf1fcf181a11fa7d8fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766546"
---
# <a name="feid"></a><span data-ttu-id="bd6d1-103">FEID</span><span class="sxs-lookup"><span data-stu-id="bd6d1-103">FEID</span></span>

 
  
<span data-ttu-id="bd6d1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd6d1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd6d1-105">Identificador de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="bd6d1-105">Identifier for a folder.</span></span> <span data-ttu-id="bd6d1-106">Ele contém um identificador de entrada e outras informações relevantes.</span><span class="sxs-lookup"><span data-stu-id="bd6d1-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bd6d1-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="bd6d1-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="bd6d1-108">Membros</span><span class="sxs-lookup"><span data-stu-id="bd6d1-108">Members</span></span>

 <span data-ttu-id="bd6d1-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="bd6d1-109">_abFlags_</span></span>
  
> <span data-ttu-id="bd6d1-110">Identificador de entrada de 4 bytes para a pasta.</span><span class="sxs-lookup"><span data-stu-id="bd6d1-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="bd6d1-111">Para obter mais informações sobre identificadores de entrada MAPI, consulte **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="bd6d1-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="bd6d1-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="bd6d1-112">_muid_</span></span>
  
> <span data-ttu-id="bd6d1-113">GUID que identifica o provedor de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bd6d1-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="bd6d1-114">Consulte mapidefs.h para a definição de tipo de **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="bd6d1-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="bd6d1-115">_espaço reservado_</span><span class="sxs-lookup"><span data-stu-id="bd6d1-115">_placeholder_</span></span>
  
> <span data-ttu-id="bd6d1-116">Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="bd6d1-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="bd6d1-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="bd6d1-117">_ltid_</span></span>
  
> <span data-ttu-id="bd6d1-118">ID de longo prazo da pasta.</span><span class="sxs-lookup"><span data-stu-id="bd6d1-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd6d1-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd6d1-119">See also</span></span>



[<span data-ttu-id="bd6d1-120">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="bd6d1-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="bd6d1-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="bd6d1-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="bd6d1-122">LTID</span><span class="sxs-lookup"><span data-stu-id="bd6d1-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="bd6d1-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="bd6d1-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="bd6d1-124">SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="bd6d1-124">SYNC</span></span>](sync.md)

