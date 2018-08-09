---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Modificado pela última vez: 03 de julho de 2012'
ms.openlocfilehash: 1b725dc5151f1f088f2547a1ef82d322c8458b6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768150"
---
# <a name="meid"></a>MEID

 
  
**Aplica-se a**: Outlook 
  
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

## <a name="members"></a>Members

 _abFlags_
  
> Identificador de entrada de 4 bytes do item do Outlook. Para obter mais informações sobre identificadores de entrada MAPI, consulte **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID que identifica o provedor de armazenamento. Consulte mapidefs.h para a definição de tipo de **MAPIUID**. 
    
 _espaço reservado_
  
> Este membro é reservado para uso interno do Outlook e não é suportado.
    
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

