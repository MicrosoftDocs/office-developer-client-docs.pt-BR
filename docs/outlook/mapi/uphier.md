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
ms.openlocfilehash: a1ec71d7120eab220ee3b11d2a751fba51cee48e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592091"
---
# <a name="uphier"></a>UPHIER
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para a sincronização de uma hierarquia de pastas durante o [carregamento do estado de hierarquia](upload-hierarchy-state.md).
  
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
  
> [in] Sinalizadores para modificar o comportamento durante a sincronização de hierarquia de pastas.
    
  - UPH_OK
    
    - [in] Carregamento foi bem-sucedida. O cliente define esta após carregar com êxito as informações para o servidor. Após a vejam esse sinalizador, Outlook limpa qualquer informação de escrituração contábil interna que indicado que na hierarquia de pastas precisava ser atualizada. 
    
    - O cliente passa o HRESULT, se o carregamento não foi bem-sucedida.
    
_pstmReserved_
  
> [out] Este membro é reservado para uso interno do Outlook e não é suportado.
    
_iEnt_
  
> [out] Índice para controlar o número de pastas especificadas pela *cEnt* como sincronizar. 
    
_cEnt_
  
> [out] Número de pastas que estão fora de sincronia.
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md)
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes de MAPI](mapi-constants.md)

