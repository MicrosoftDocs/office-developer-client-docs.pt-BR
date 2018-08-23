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
ms.openlocfilehash: 29dd2e3b47d0f43df7824274d2fdcc4f7f16eeb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569852"
---
# <a name="ltid"></a>LTID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

