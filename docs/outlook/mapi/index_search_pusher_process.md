---
title: INDEX_SEARCH_PUSHER_PROCESS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6b39504f-6eed-2605-048d-2707f38a7d9a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9495caecd514656f6fd62fb5db6cd8ac2faf4b50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581738"
---
# <a name="indexsearchpusherprocess"></a>INDEX_SEARCH_PUSHER_PROCESS

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica o processo que está enviando uma notificação para o manipulador de protocolo MAPI que um objeto desse repositório está pronto para indexação.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a>Members

 *dwPID* 
  
>  ID de processo para o processo que está enviando uma notificação de indexação para o indexador do manipulador de protocolo de MAPI. 
    

