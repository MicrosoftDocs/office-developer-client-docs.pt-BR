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
ms.openlocfilehash: f6afa890f61bb2f394e3cf69e0f2c54699a2ad9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770293"
---
# <a name="rtfsync"></a>RTFSync

**Aplica-se a**: Outlook 
  
Certifica-se de que o texto da mensagem de Rich Text Format (RTF) corresponda à versão de texto sem formatação. É necessário chamar essa função antes de ler a versão RTF e depois de modificar a versão RTF. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de armazenamento de mensagem e aplicativos cliente com reconhecimento de RTF  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>Parâmetros

_lpMessage_
  
> [in] Ponteiro para a mensagem a ser atualizado.
    
_ulFlags_
  
> [in] Bitmask dos sinalizadores usados para indicar o RTF ou a versão de texto sem formatação da mensagem foi alterada. Sinalizadores a seguir podem ser definidos:
    
  - RTF_SYNC_BODY_CHANGED: A versão de texto sem formatação da mensagem foi alterada.
      
  - RTF_SYNC_RTF_CHANGED: A versão RTF da mensagem foi alterada.
    
  Todos os outros bits no parâmetro _ulFlags_ são reservados para uso futuro. 
    
_lpfMessageUpdated_
  
> [out] Ponteiro para uma variável que indica se há uma mensagem atualizada. TRUE se não houver uma mensagem atualizada, FALSE caso contrário.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Se a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) está ausente ou é FALSE, antes de ler a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) a função **RTFSync** deve ser chamado com o RTF_SYNC_BODY_ ALTERADO o sinalizador definido. 
  
Se o sinalizador STORE_RTF_OK não estiver definido na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), essa função deve ser chamada com o sinalizador RTF_SYNC_RTF_CHANGED definido depois de modificar **PR_RTF_COMPRESSED**. 
  
Se **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) e o **PR_RTF_COMPRESSED** foram alterados, a função **RTFSync** deve ser chamada com os dois conjuntos de sinalizadores. 
  
Se o valor do parâmetro _lpfMessageUpdated_ for definido como TRUE, o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) deve ser chamado para a mensagem. Se **SaveChanges** não for chamado, as modificações não serão salvas na mensagem. 
  
Provedores de armazenamento de mensagens podem usar **RTFSync** para manter as propriedades **PR_BODY** e **PR_RTF_COMPRESSED** sincronizadas. 
  
Para obter mais informações, consulte [Com suporte para texto de RTF para provedores de armazenamento de mensagem](supporting-rtf-text-for-message-store-providers.md). 
  
## <a name="see-also"></a>Confira também

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)

