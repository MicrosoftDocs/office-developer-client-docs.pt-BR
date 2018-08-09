---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e281907931a493e82c44913a7c26f6df55876e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770685"
---
# <a name="upmsg"></a>UPMSG

**Aplica-se a**: Outlook 
  
Informações de carregamento de um item do Outlook durante o [carregamento do estado da mensagem](upload-message-state.md).
  
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

## <a name="members"></a>Members

 _ulFlags_
  
> [out] / [in] sinalizadores para determinar o comportamento apropriado durante o carregamento. 
    
  - UPM_ASSOC
    
    - [out] Item está associado.
    
  - UPM_NEW
    
    - [out] Novo item. 
    
  - UPM_MOV
    
    - [out] Item foi movido aqui.
    
  - UPM_MOD_PROPS
    
    - [out] Propriedades do item foram modificadas.
    
  - UPM_HEADER
    
    - [out] O item é o cabeçalho da mensagem.
    
  - UPM_OK
    
    - [in] Carregamento foi bem-sucedida. O cliente define esta após carregar as informações para o servidor.
    
  - UPM_MOVED
    
    - [in] Item foi movido com êxito.
    
  - UPM_COMMIT
    
    - [in] Confirme o estado de carregamento agora.
    
  - UPM_DELETE
    
    - [in] Exclua item agora.
    
  - UPM_SAVE
    
    - [in] Salve alterações no item.
    
_pmsg_
  
> [out] Objeto de item aberto. Consulte mapidefs.h para a definição de tipo de **LPMESSAGE**. 
    
_meid_
  
> [out] Identificação de entrada do item.
    
_binReserved1_
  
> [in] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_binReserved2_
  
> [in] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_feid_
  
> [out] Identificação de entrada da pasta de origem, se o item foi movido.
    
_binChg_
  
> [out] Alterar chave do item de destino, se o item foi movido. Consulte mapidefs.h para a definição de tipo de **SBinary**. 
    
_binPcl_
  
> [out] Alterar a lista do item de destino, se o item foi movido. Consulte mapidefs.h para a definição de tipo de **SBinary**. 
    
_skeySrc_
  
> [out] Chave de origem do item de origem, se o item foi movido.
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md)
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [FEID](feid.md)
- [MEID](meid.md)
- [SKEY](skey.md)

