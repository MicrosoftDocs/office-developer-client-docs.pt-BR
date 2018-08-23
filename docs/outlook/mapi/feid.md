---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Modificado pela última vez: 02 de julho de 2012'
ms.openlocfilehash: 3e534f91863e2a1300e03d112d1f532f486eedd9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588304"
---
# <a name="feid"></a>FEID

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Identificador de uma pasta. Ele contém um identificador de entrada e outras informações relevantes.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a>Members

 _abFlags_
  
> Identificador de entrada de 4 bytes para a pasta. Para obter mais informações sobre identificadores de entrada MAPI, consulte **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID que identifica o provedor de armazenamento. Consulte mapidefs.h para a definição de tipo de **MAPIUID**. 
    
 _espaço reservado_
  
> Este membro é reservado para uso interno do Outlook e não é suportado.
    
 _ltid_
  
> ID de longo prazo da pasta.
    
## <a name="see-also"></a>Confira também



[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SYNC](sync.md)

