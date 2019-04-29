---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2ea877c9328279322de0f15e5755096e74819425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419433"
---
# <a name="ltid"></a>LTID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
ID de longo prazo genérico de um objeto em um repositório do Outlook.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a>Membros

 _guid_
  
- bota O GUID do servidor que criou o objeto.
    
 _globcnt_
  
- bota Um número exclusivo de 6 bytes que identifica o objeto no repositório do Outlook.
    
 _wLevel_
  
- bota O nível de hierarquia da ID de entrada para uma pasta pública favorita do Exchange.
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[FEID](feid.md)

