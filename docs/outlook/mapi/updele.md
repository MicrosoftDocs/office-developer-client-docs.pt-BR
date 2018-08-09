---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4dd60ffe305d27db2c9118e11cccf692652d0d27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770664"
---
# <a name="updele"></a>UPDELE

**Aplica-se a**: Outlook 
  
Informações para itens que foram excluídos em um repositório local estendidas. Essas informações são usadas durante o [carregamento excluir o estado de status](upload-delete-status-state.md).
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPDELE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
    DWORD   dwReserved; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeyDst; 
    PUPMOV pupmov; 
};
```

## <a name="members"></a>Members

_ulFlags_
  
> [out] / [in] sinalizadores para determinar o comportamento apropriado durante o carregamento.
    
  - UPD_ASSOC
    
    - [out] Item está associado.
    
  - UPD_MOV
    
    - [out] Item foi movido check-out.
    
  - UPD_OK 
    
    - [in] Carregamento foi bem-sucedida. O cliente define esta após carregar informações ao servidor.
    
  - UPD_MOVED
    
    - [in] Item foi movido com êxito.
    
  - UPD_UPDATE
    
    - [in] Item de fonte de marca como modificado.
    
  - UPD_COMMIT
    
    - [in] Confirme o estado de carregamento agora (entrada de 0).
    
_skey_
  
> [out] Chave de origem do item.
    
_dwReserved_
  
> [out] Este membro é reservado para uso interno do Outlook e não é suportado.
    
_binChg_
  
> [out] Alterar chave de item de destino se o item foi movido.
    
_binPcl_
  
> [out] Alterar a lista de item de destino se o item foi movido.
    
_skeyDst_
  
> [out] Chave de origem do item de destino se o item foi movida.
    
_pupmov_
  
> [out] Informações da pasta de destino se o item foi movidas.
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md) 
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

