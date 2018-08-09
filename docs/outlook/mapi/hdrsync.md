---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: bd1c327eb2042957c8fb043736950af3dae520b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766696"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**Aplica-se a**: Outlook 
  
Informações para sincronizar o cabeçalho da mensagem durante a [baixar o estado do cabeçalho da mensagem](download-message-header-state.md).
  
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

## <a name="members"></a>Members

 _pupmsg_
  
- [out] Informações de cabeçalho da mensagem atual no armazenamento local.
    
 _feidPar_
  
- [out] Identificação de entrada para a pasta pai do item de mensagem.
    
 _pstmReserved_
  
- [out] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
 _ulFlags_
  
- [in] Sinalizadores para modificar o comportamento:
    
- HSF_LOCAL
    
  - [in] Item completo reside no mesmo armazenamento local como o item de cabeçalho.
    
- HSF_COPYDESTRUCTIVE
    
  -  [in] Otimize as operações de cópia interna. Isso pode causar perda de dados. **HSF_LOCAL** deve ser definida. 
    
- HSF_OK
    
  - [in] Sincronização de cabeçalho foi bem-sucedida. O cliente define esta após fazer o download de informações do servidor.
    
     _pmsgFull_
    
  - [in] O item de mensagem completo, incluindo o cabeçalho da mensagem é baixado do servidor. Consulte mapidefs.h para a definição de tipo de **LPMESSAGE**. 
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[FEID](feid.md)

