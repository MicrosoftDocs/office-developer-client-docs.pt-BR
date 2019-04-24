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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342781"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para sincronizar um cabeçalho de mensagem durante o [download do estado do cabeçalho da mensagem](download-message-header-state.md).
  
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

 _pupmsg_
  
- bota Informações do cabeçalho da mensagem atual no repositório local.
    
 _feidPar_
  
- bota ID de entrada da pasta pai do item de mensagem.
    
 _pstmReserved_
  
- [uto] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
 _ulFlags_
  
- no Sinalizadores para modificar o comportamento:
    
- HSF_LOCAL
    
  - no O item completo reside no mesmo repositório local que o item de cabeçalho.
    
- HSF_COPYDESTRUCTIVE
    
  -  no Otimizar operações de cópia interna. Isso pode causar perda de dados. **HSF_LOCAL** deve ser definido. 
    
- HSF_OK
    
  - no A sincronização do cabeçalho foi bem-sucedida. O cliente define isso depois de baixar informações do servidor.
    
     _pmsgFull_
    
  - no O item de mensagem completo, incluindo o cabeçalho da mensagem baixado do servidor. Consulte mapidefs. h para a definição de tipo de **lpMessage**. 
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes de MAPI](mapi-constants.md)
  
[FEID](feid.md)

