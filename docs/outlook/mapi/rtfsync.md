---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dfdf1068caaab3894b1b489d53ccc8debe1b3a29
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436206"
---
# <a name="rtfsync"></a>RTFSync

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Verifica se o texto da mensagem RTF (Rich Text Format) corresponde à versão de texto sem formatação. É necessário chamar essa função antes de ler a versão RTF e depois de modificar a versão RTF. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos clientes com reconhecimento de RTF e provedores de repositórios de mensagens  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>Parâmetros

_lpMessage_
  
> no Ponteiro para a mensagem a ser atualizada.
    
_ulFlags_
  
> no Bitmask dos sinalizadores usados para indicar que a versão em RTF ou texto sem formatação da mensagem foi alterada. Os seguintes sinalizadores podem ser definidos:
    
  - RTF_SYNC_BODY_CHANGED: a versão de texto sem formatação da mensagem foi alterada.
      
  - RTF_SYNC_RTF_CHANGED: a versão RTF da mensagem foi alterada.
    
  Todos os outros bits no parâmetro _parâmetroulflags_ são reservados para uso futuro. 
    
_lpfMessageUpdated_
  
> bota Ponteiro para uma variável que indica se há uma mensagem atualizada. TRUE se houver uma mensagem atualizada; caso contrário, FALSE.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Se a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) estiver ausente ou for false, antes de ler a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), a função **RTFSync** deverá ser chamada com o RTF_SYNC_BODY_ Conjunto de sinalizadores alterado. 
  
Se o sinalizador STORE_RTF_OK não estiver definido na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), essa função deverá ser chamada com o sinalizador RTF_SYNC_RTF_CHANGED definido após a modificação de **PR_RTF_COMPRESSED**. 
  
Se ambos os **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) e **PR_RTF_COMPRESSED** tiverem sido alterados, a função **RTFSync** deverá ser chamada com ambos os sinalizadores definidos. 
  
Se o valor do parâmetro _lpfMessageUpdated_ for definido como true, o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) deverá ser chamado para a mensagem. Se **SaveChanges** não for chamado, as modificações não serão salvas na mensagem. 
  
Os provedores de repositórios de mensagens podem usar o **RTFSync** para manter as propriedades **PR_BODY** e **PR_RTF_COMPRESSED** sincronizadas. 
  
Para obter mais informações, consulte [suporte a texto RTF para provedores de repositório de mensagens](supporting-rtf-text-for-message-store-providers.md). 
  
## <a name="see-also"></a>Confira também

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)

