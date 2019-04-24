---
title: SYNCSTATE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 63c47e94-f603-aef9-afed-e3819bd79408
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 64348347ea930e6a6a80b9a9075299d2e3109eda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360701"
---
# <a name="syncstate"></a><span data-ttu-id="e37fd-103">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="e37fd-103">SYNCSTATE</span></span>

<span data-ttu-id="e37fd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e37fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e37fd-105">Essa estrutura define os Estados da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="e37fd-105">This structure defines the states for the replication state machine.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e37fd-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="e37fd-106">Quick info</span></span>

```cpp
typedef enum { 
    LR_SYNC_IDLE = 0, 
    LR_SYNC, 
    LR_SYNC_UPLOAD_HIERARCHY, 
    LR_SYNC_UPLOAD_FOLDER, 
    LR_SYNC_CONTENTS, 
    LR_SYNC_UPLOAD_TABLE, 
    LR_SYNC_UPLOAD_MESSAGE, 
    LR_SYNC_UPLOAD_MESSAGE_READ = 8, 
    LR_SYNC_UPLOAD_MESSAGE_DEL, 
    LR_SYNC_DOWNLOAD_HIERARCHY, 
    LR_SYNC_DOWNLOAD_TABLE, 
    LR_SYNC_DOWNLOAD_HEADER = 17 
} SYNCSTATE; 

```

## <a name="see-also"></a><span data-ttu-id="e37fd-107">Confira também</span><span class="sxs-lookup"><span data-stu-id="e37fd-107">See also</span></span>

- [<span data-ttu-id="e37fd-108">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="e37fd-108">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="e37fd-109">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="e37fd-109">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="e37fd-110">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="e37fd-110">MAPI Constants</span></span>](mapi-constants.md)

