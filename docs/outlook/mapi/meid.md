---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Última modificação: 03 de julho de 2012'
ms.openlocfilehash: a9aea0db700de9c82aa2a41a443ebf03da8ce9b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356970"
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
  
> identificador de entrada de 4 bytes para o item do Outlook. Para obter mais informações sobre identificadores de entrada MAPI **[](entryid.md)**, consulte EntryID. 
    
 _muid_
  
> GUID que identifica o provedor de repositório. Consulte mapidefs. h para a definição de tipo de **MAPIUID**. 
    
 _espaço reservado_
  
> Este membro é reservado para uso interno do Outlook e não tem suporte.
    
 _ltidFld_
  
> ID de longo prazo da pasta.
    
 _ltidMsg_
  
> ID de longo prazo do item do Outlook.
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[SINCRONIZAÇÃO](sync.md)
  
[UPMSG](upmsg.md)

