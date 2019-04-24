---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Última modificação: 02 de julho de 2012'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334836"
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
  
> identificador de entrada de 4 bytes para a pasta. Para obter mais informações sobre identificadores de entrada MAPI **[](entryid.md)**, consulte EntryID. 
    
 _muid_
  
> GUID que identifica o provedor de repositório. Consulte mapidefs. h para a definição de tipo de **MAPIUID**. 
    
 _espaço reservado_
  
> Este membro é reservado para uso interno do Outlook e não tem suporte.
    
 _ltid_
  
> ID de longo prazo da pasta.
    
## <a name="see-also"></a>Confira também



[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes de MAPI](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SINCRONIZAÇÃO](sync.md)

