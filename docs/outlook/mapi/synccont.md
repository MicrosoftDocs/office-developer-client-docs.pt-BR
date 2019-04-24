---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: afba7fa718a35d33966d45289461313e349ef2e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349571"
---
# <a name="synccont"></a>SYNCCONT

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para sincronizar o conteúdo de pastas especificadas em um repositório local com o servidor durante o [estado de sincronização do conteúdo](synchronize-contents-state.md). Isso envolve apenas upload ou uma sincronização completa envolvendo um upload e, em seguida, um download.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct SYNCCONT 
{ 
   ULONG   ulFlags; 
   UINT   iEnt; 
   UINT   cEnt; 
   LPVOID    pvReserved; 
   LPSPropTagArray   ptagaReserved; 
   LPSSortOrderSet   psosReserved; 
};
```

## <a name="members"></a>Membros

_ulFlags_
  
> no Sinalizadores para determinar o comportamento apropriado durante a sincronização.
    
  - UPC_OK
    
  - no O carregamento ou a sincronização completa foi bem-sucedido. O cliente define isso após sincronizar as informações com o servidor.
    
_iEnt_
  
> bota Índice para controlar a sincronização do conteúdo no número de pastas especificado por _cento_.
    
_cEnt_
  
> bota Número de pastas a serem replicadas.
    
_pvReserved_
  
> Este membro é reservado para uso interno do Outlook e não tem suporte. 
    
_ptagaReserved_
  
> Este membro é reservado para uso interno do Outlook e não tem suporte. 
    
_psosReserved_
  
> Este membro é reservado para uso interno do Outlook e não tem suporte. 
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md)
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes de MAPI](mapi-constants.md)

