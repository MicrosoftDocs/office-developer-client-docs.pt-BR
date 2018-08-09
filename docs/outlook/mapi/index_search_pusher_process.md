---
title: INDEX_SEARCH_PUSHER_PROCESS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6b39504f-6eed-2605-048d-2707f38a7d9a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ada6d4127d503aae0b068d40d2bb48cb6b833ea0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767551"
---
# <a name="indexsearchpusherprocess"></a><span data-ttu-id="f6f4f-103">INDEX_SEARCH_PUSHER_PROCESS</span><span class="sxs-lookup"><span data-stu-id="f6f4f-103">INDEX_SEARCH_PUSHER_PROCESS</span></span>

  
  
<span data-ttu-id="f6f4f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f6f4f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f6f4f-105">Especifica o processo que está enviando uma notificação para o manipulador de protocolo MAPI que um objeto desse repositório está pronto para indexação.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-105">Specifies the process that is sending a notification to the MAPI Protocol Handler that an object in that store is ready for indexing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f6f4f-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="f6f4f-106">Quick info</span></span>

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a><span data-ttu-id="f6f4f-107">Members</span><span class="sxs-lookup"><span data-stu-id="f6f4f-107">Members</span></span>

 <span data-ttu-id="f6f4f-108">*dwPID*</span><span class="sxs-lookup"><span data-stu-id="f6f4f-108">*dwPID*</span></span> 
  
>  <span data-ttu-id="f6f4f-109">ID de processo para o processo que está enviando uma notificação de indexação para o indexador do manipulador de protocolo de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f6f4f-109">Process ID for the process that is sending an indexing notification to the indexer of the MAPI Protocol Handler.</span></span> 
    

