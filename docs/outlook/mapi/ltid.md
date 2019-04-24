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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357411"
---
# <a name="ltid"></a><span data-ttu-id="1521f-103">LTID</span><span class="sxs-lookup"><span data-stu-id="1521f-103">LTID</span></span>

  
  
<span data-ttu-id="1521f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1521f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1521f-105">ID de longo prazo genérico de um objeto em um repositório do Outlook.</span><span class="sxs-lookup"><span data-stu-id="1521f-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1521f-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="1521f-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="1521f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1521f-107">Members</span></span>

 <span data-ttu-id="1521f-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="1521f-108">_guid_</span></span>
  
- <span data-ttu-id="1521f-109">bota O GUID do servidor que criou o objeto.</span><span class="sxs-lookup"><span data-stu-id="1521f-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="1521f-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="1521f-110">_globcnt_</span></span>
  
- <span data-ttu-id="1521f-111">bota Um número exclusivo de 6 bytes que identifica o objeto no repositório do Outlook.</span><span class="sxs-lookup"><span data-stu-id="1521f-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="1521f-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="1521f-112">_wLevel_</span></span>
  
- <span data-ttu-id="1521f-113">bota O nível de hierarquia da ID de entrada para uma pasta pública favorita do Exchange.</span><span class="sxs-lookup"><span data-stu-id="1521f-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1521f-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="1521f-114">See also</span></span>



[<span data-ttu-id="1521f-115">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="1521f-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="1521f-116">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="1521f-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="1521f-117">FEID</span><span class="sxs-lookup"><span data-stu-id="1521f-117">FEID</span></span>](feid.md)

