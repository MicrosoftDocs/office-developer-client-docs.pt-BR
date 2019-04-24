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
ms.openlocfilehash: 64e5cf31dffdc794a22bcbd6d503a2b688f9c733
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332204"
---
# <a name="indexsearchpusherprocess"></a>INDEX_SEARCH_PUSHER_PROCESS

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica o processo que está enviando uma notificação para o manipulador de protocolo MAPI de que um objeto no repositório está pronto para indexação.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a>Membros

 *dwPID* 
  
>  ID do processo que está enviando uma notificação de indexação para o indexador do manipulador de protocolo MAPI. 
    

