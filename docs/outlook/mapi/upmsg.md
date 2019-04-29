---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1e0e2f9b794c4cee25488a754290922e58b7658d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427266"
---
# <a name="upmsg"></a>UPMSG

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para carregar um item do Outlook durante o [estado de mensagem de carregamento](upload-message-state.md).
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPMSG 
{ 
    ULONG ulFlags; 
    LPMESSAGE pmsg; 
    MEID meid; 
    SBinary binReserved1; 
    SBinary binReserved2; 
    FEID feid; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeySrc; 
};
```

## <a name="members"></a>Membros

 _ulFlags_
  
> [out]/[in] flags para determinar o comportamento apropriado durante o carregamento. 
    
  - UPM_ASSOC
    
    - bota Item está associado.
    
  - UPM_NEW
    
    - bota Novo item. 
    
  - UPM_MOV
    
    - bota O item foi movido aqui.
    
  - UPM_MOD_PROPS
    
    - bota As propriedades do item foram modificadas.
    
  - UPM_HEADER
    
    - bota Item é um cabeçalho de mensagem.
    
  - UPM_OK
    
    - no O upload foi bem-sucedido. O cliente define isso após carregar informações no servidor.
    
  - UPM_MOVED
    
    - no O item foi movido com êxito.
    
  - UPM_COMMIT
    
    - no Confirme o estado de carregamento agora.
    
  - UPM_DELETE
    
    - no Excluir o item agora.
    
  - UPM_SAVE
    
    - no Salvar alterações no item.
    
_pMsg_
  
> bota Objeto Open item. Consulte mapidefs. h para a definição de tipo de **lpMessage**. 
    
_MEID_
  
> bota ID de entrada do item.
    
_binReserved1_
  
> no Este membro é reservado para uso interno do Outlook e não tem suporte. 
    
_binReserved2_
  
> no Este membro é reservado para uso interno do Outlook e não tem suporte. 
    
_feid_
  
> bota ID de entrada da pasta de origem, se o item foi movido.
    
_binChg_
  
> bota Altere a chave do item de destino, se o item foi movido. Consulte mapidefs. h para a definição de tipo de **SBinary**. 
    
_binPcl_
  
> bota Altere a lista do item de destino, se o item foi movido. Consulte mapidefs. h para a definição de tipo de **SBinary**. 
    
_skeySrc_
  
> bota Chave de origem do item de origem, se o item foi movido.
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md)
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes de MAPI](mapi-constants.md)
- [FEID](feid.md)
- [MEID](meid.md)
- [SKEY](skey.md)

