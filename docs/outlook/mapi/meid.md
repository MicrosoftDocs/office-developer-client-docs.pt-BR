---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: a9aea0db700de9c82aa2a41a443ebf03da8ce9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430305"
---
# <a name="meid"></a>MEID

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Identificador de um item do Outlook. Ele contém um identificador de entrada e outras informações relevantes.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct MEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltidFld; 
    LTID ltidMsg; 
};
```

## <a name="members"></a>Membros

 _abFlags_
  
> Identificador de entrada de 4 byte para o item do Outlook. Para obter mais informações sobre identificadores de entrada MAPI, consulte **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID que identifica o provedor do armazenamento. Consulte mapidefs.h para a definição de tipo de **MAPIUID**. 
    
 _espaço reservado_
  
> Este membro está reservado para uso interno do Outlook e não tem suporte.
    
 _ltidFld_
  
> ID de longo prazo da pasta.
    
 _ltidMsg_
  
> ID de longo prazo do item do Outlook.
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[SYNC](sync.md)
  
[UPMSG](upmsg.md)

