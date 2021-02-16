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
ms.openlocfilehash: 9bd61739b14d0ec382a9d582689c1049fe89429b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424879"
---
# <a name="updele"></a>UPDELE

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações estendidas para itens que foram excluídos em um armazenamento local. Essas informações são usadas durante o [estado de status de exclusão de upload.](upload-delete-status-state.md)
  
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
  
> [out]/[in] Sinalizadores para determinar o comportamento apropriado durante o carregamento.
    
  - UPD_ASSOC
    
    - [out] Item está associado.
    
  - UPD_MOV
    
    - [out] Item foi movido para fora.
    
  - UPD_OK 
    
    - [in] O carregamento foi bem-sucedido. O cliente define isso depois de carregar informações no servidor.
    
  - UPD_MOVED
    
    - [in] Item foi movido com êxito.
    
  - UPD_UPDATE
    
    - [in] Marque o item de origem como modificado.
    
  - UPD_COMMIT
    
    - [in] Confirma o estado de carregamento agora (entrada 0).
    
_skey_
  
> [out] Chave de origem do item.
    
_dwReserved_
  
> [out] Esse membro é reservado para uso interno do Outlook e não tem suporte.
    
_binChg_
  
> [out] Alterar a chave do item de destino se o item tiver sido movido.
    
_binPcl_
  
> [out] Alterar a lista de itens de destino se o item tiver sido movido.
    
_skeyDst_
  
> [out] Chave de origem do item de destino se o item tiver sido movido.
    
_realizoumov_
  
> [out] Informações da pasta de destino se o item tiver sido movido.
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md) 
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes de MAPI](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

