---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f4ece0662b72047b785b03f3134c96fac48c219a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770436"
---
# <a name="skey"></a>SKEY

  
  
**Aplica-se a**: Outlook 
  
Chave de origem para um item do Outlook.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a>Members

 _guid_
  
> GUID do servidor criando o objeto.
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[UPDELE](updele.md)
  
[UPMSG](upmsg.md)
  
[UPREADE](upreade.md)

