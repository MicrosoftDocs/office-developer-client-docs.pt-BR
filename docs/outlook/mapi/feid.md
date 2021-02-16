---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409808"
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

## <a name="members"></a>Membros

 _abFlags_
  
> Identificador de entrada de 4 byte para a pasta. Para obter mais informações sobre identificadores de entrada MAPI, consulte **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID que identifica o provedor do armazenamento. Consulte mapidefs.h para a definição de tipo de **MAPIUID**. 
    
 _espaço reservado_
  
> Este membro está reservado para uso interno do Outlook e não tem suporte.
    
 _ltid_
  
> ID de longo prazo da pasta.
    
## <a name="see-also"></a>Confira também



[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes de MAPI](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SYNC](sync.md)

