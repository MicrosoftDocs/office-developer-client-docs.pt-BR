---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2361d225c07d60fab40465b27ad393ca10f6d8eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566583"
---
# <a name="updele"></a>UPDELE

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Membros

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
  
> [out] Esse membro é reservado para uso interno do Outlook e não tem suporte.
    
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
- [Constantes de MAPI](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

