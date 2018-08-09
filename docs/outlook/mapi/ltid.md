---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4a60e2fe3a58e1d696ae9645e03ce8dde5340d9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767778"
---
# <a name="ltid"></a><span data-ttu-id="c501f-103">LTID</span><span class="sxs-lookup"><span data-stu-id="c501f-103">LTID</span></span>

  
  
<span data-ttu-id="c501f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c501f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c501f-105">ID de termos longos genérico de um objeto em um armazenamento do Outlook.</span><span class="sxs-lookup"><span data-stu-id="c501f-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c501f-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="c501f-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="c501f-107">Members</span><span class="sxs-lookup"><span data-stu-id="c501f-107">Members</span></span>

 <span data-ttu-id="c501f-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="c501f-108">_guid_</span></span>
  
- <span data-ttu-id="c501f-109">[out] O GUID do servidor que criou o objeto.</span><span class="sxs-lookup"><span data-stu-id="c501f-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="c501f-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="c501f-110">_globcnt_</span></span>
  
- <span data-ttu-id="c501f-111">[out] Um número exclusivo de 6 bytes que identifica o objeto dentro do repositório do Outlook.</span><span class="sxs-lookup"><span data-stu-id="c501f-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="c501f-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="c501f-112">_wLevel_</span></span>
  
- <span data-ttu-id="c501f-113">[out] O nível da hierarquia da identificação de entrada para uma pasta pública Favoritos do Exchange.</span><span class="sxs-lookup"><span data-stu-id="c501f-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c501f-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="c501f-114">See also</span></span>



[<span data-ttu-id="c501f-115">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="c501f-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="c501f-116">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="c501f-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="c501f-117">FEID</span><span class="sxs-lookup"><span data-stu-id="c501f-117">FEID</span></span>](feid.md)

