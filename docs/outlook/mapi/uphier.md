---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414918"
---
# <a name="uphier"></a>UPHIER
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para sincronizar uma hierarquia de pastas durante o [estado de hierarquia de upload](upload-hierarchy-state.md).
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a>Membros

_ulFlags_
  
> no Sinalizadores para modificar o comportamento ao sincronizar a hierarquia de pastas.
    
  - UPH_OK
    
    - no O upload foi bem-sucedido. O cliente define isso após carregar as informações com êxito no servidor. Ao ver esse sinalizador, o Outlook limpa todas as informações de escrituração interna que indicaram que a hierarquia de pastas precisava ser atualizada. 
    
    - O cliente passa o HRESULT se o upload não tiver sido bem-sucedido.
    
_pstmReserved_
  
> bota Este membro é reservado para uso interno do Outlook e não tem suporte.
    
_iEnt_
  
> bota Índice para controlar a sincronização do número de pastas especificado por *cento* . 
    
_cEnt_
  
> bota Número de pastas que estão fora de sincronia.
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md)
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes de MAPI](mapi-constants.md)

