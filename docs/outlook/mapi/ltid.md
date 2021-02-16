---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2ea877c9328279322de0f15e5755096e74819425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419433"
---
# <a name="ltid"></a><span data-ttu-id="2fc9f-103">LTID</span><span class="sxs-lookup"><span data-stu-id="2fc9f-103">LTID</span></span>

  
  
<span data-ttu-id="2fc9f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fc9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fc9f-105">ID genérica de longo prazo de um objeto em um armazenamento do Outlook.</span><span class="sxs-lookup"><span data-stu-id="2fc9f-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2fc9f-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="2fc9f-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="2fc9f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2fc9f-107">Members</span></span>

 <span data-ttu-id="2fc9f-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="2fc9f-108">_guid_</span></span>
  
- <span data-ttu-id="2fc9f-109">[out] O GUID do servidor que criou o objeto.</span><span class="sxs-lookup"><span data-stu-id="2fc9f-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="2fc9f-110">_bcnt_</span><span class="sxs-lookup"><span data-stu-id="2fc9f-110">_globcnt_</span></span>
  
- <span data-ttu-id="2fc9f-111">[out] Um número exclusivo de 6 byte que identifica o objeto dentro do armazenamento do Outlook.</span><span class="sxs-lookup"><span data-stu-id="2fc9f-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="2fc9f-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="2fc9f-112">_wLevel_</span></span>
  
- <span data-ttu-id="2fc9f-113">[out] O nível de hierarquia da ID de entrada de uma pasta pública favorita do Exchange.</span><span class="sxs-lookup"><span data-stu-id="2fc9f-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2fc9f-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="2fc9f-114">See also</span></span>



[<span data-ttu-id="2fc9f-115">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="2fc9f-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2fc9f-116">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="2fc9f-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2fc9f-117">FEID</span><span class="sxs-lookup"><span data-stu-id="2fc9f-117">FEID</span></span>](feid.md)

