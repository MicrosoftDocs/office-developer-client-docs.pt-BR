---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 82923895353cf600c4d0b78b9a6e16fc7d57e466
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770550"
---
# <a name="synccont"></a>SYNCCONT

**Aplica-se a**: Outlook 
  
Informações para sincronizar o conteúdo das pastas especificados em um armazenamento local com o servidor durante a [sincronizar o estado de conteúdo](synchronize-contents-state.md). Isso envolve apenas carregamento ou uma sincronização completa envolvendo um upload e download.
  
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

## <a name="members"></a>Members

_ulFlags_
  
> [in] Sinalizadores para determinar o comportamento apropriado durante a sincronização.
    
  - UPC_OK
    
  - [in] Carregar ou sincronização completa foi bem-sucedida. O cliente define isso após a sincronização de informações com o servidor.
    
_iEnt_
  
> [out] Índice para controlar a sincronização de conteúdo no número de pastas especificadas pela _cEnt_.
    
_cEnt_
  
> [out] Número de pastas a serem replicadas.
    
_pvReserved_
  
> Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_ptagaReserved_
  
> Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_psosReserved_
  
> Este membro é reservado para uso interno do Outlook e não é suportado. 
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md)
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

