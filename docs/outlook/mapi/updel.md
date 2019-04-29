---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c9d2ec7f1970e3d1cadb65ab9af360b5c01c6844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436794"
---
# <a name="updel"></a><span data-ttu-id="29bc6-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="29bc6-103">UPDEL</span></span>

  
  
<span data-ttu-id="29bc6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29bc6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29bc6-105">Informações para itens que foram excluídos em um repositório local.</span><span class="sxs-lookup"><span data-stu-id="29bc6-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="29bc6-106">Essas informações são usadas durante o [estado de status de exclusão de upload](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="29bc6-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="29bc6-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="29bc6-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="29bc6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="29bc6-108">Members</span></span>

 <span data-ttu-id="29bc6-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="29bc6-109">_pupde_</span></span>
  
>  <span data-ttu-id="29bc6-110">bota Vetor de entradas de [UPDELE](updele.md) .</span><span class="sxs-lookup"><span data-stu-id="29bc6-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="29bc6-111">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="29bc6-111">_cEnt_</span></span>
  
> <span data-ttu-id="29bc6-112">bota Número de entradas no *pupde* .</span><span class="sxs-lookup"><span data-stu-id="29bc6-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="29bc6-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="29bc6-113">See also</span></span>



[<span data-ttu-id="29bc6-114">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="29bc6-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="29bc6-115">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="29bc6-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="29bc6-116">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="29bc6-116">MAPI Constants</span></span>](mapi-constants.md)

