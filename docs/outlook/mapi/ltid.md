---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4a60e2fe3a58e1d696ae9645e03ce8dde5340d9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767778"
---
# <a name="ltid"></a>LTID

  
  
**Aplica-se a**: Outlook 
  
ID de termos longos genérico de um objeto em um armazenamento do Outlook.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a>Members

 _guid_
  
- [out] O GUID do servidor que criou o objeto.
    
 _globcnt_
  
- [out] Um número exclusivo de 6 bytes que identifica o objeto dentro do repositório do Outlook.
    
 _wLevel_
  
- [out] O nível da hierarquia da identificação de entrada para uma pasta pública Favoritos do Exchange.
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[FEID](feid.md)

