---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2131197ca24804eec74270100fa70c05c47a27cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410249"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para sincronizar um header de mensagem durante o estado [de download do header da mensagem.](download-message-header-state.md)
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct HDRSYNC 
{ 
    UPMSG *pupmsg; 
    FEID feidPar; 
    LPSTREAM pstmReserved; 
    ULONG ulFlags; 
    LPMESSAGE pmsgFull; 
};
```

## <a name="members"></a>Membros

 _btmsg_
  
- [out] Informações para o header de mensagem atual no armazenamento local.
    
 _feidPar_
  
- [out] Entry ID for the parent folder of the message item.
    
 _pstmReserved_
  
- [uto] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
 _ulFlags_
  
- [in] Sinalizadores para modificar o comportamento:
    
- HSF_LOCAL
    
  - [in] O item completo reside no mesmo armazenamento local que o item de header.
    
- HSF_COPYDESTRUCTIVE
    
  -  [in] Otimizar operações de cópia interna. Isso pode causar perda de dados. **HSF_LOCAL** deve ser definido. 
    
- HSF_OK
    
  - [in] A sincronização do header foi bem-sucedida. O cliente define isso depois de baixar informações do servidor.
    
     _pmsgFull_
    
  - [in] O item de mensagem completo, incluindo o header da mensagem baixado do servidor. Consulte mapidefs.h para a definição de tipo de **LPMESSAGE**. 
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes de MAPI](mapi-constants.md)
  
[FEID](feid.md)

