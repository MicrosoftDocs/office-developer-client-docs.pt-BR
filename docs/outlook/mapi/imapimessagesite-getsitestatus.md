---
title: IMAPIMessageSiteGetSiteStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSiteStatus
api_type:
- COM
ms.assetid: 02718898-7857-4e43-8f46-622269f812e6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7d81533b13f4f44a0644215e009dc3477717e9a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767084"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**Aplica-se a**: Outlook 
  
Retorna informações de um objeto de site de mensagem sobre a mensagem de recursos do site da mensagem atual.
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parâmetros

 _lpulStatus_
  
> [out] Um ponteiro para uma bitmask dos sinalizadores que fornece informações sobre o status da mensagem. Sinalizadores a seguir podem ser definidos:
    
VCSTATUS_COPY 
  
> A mensagem pode ser copiada. 
    
VCSTATUS_DELETE 
  
> A mensagem pode ser excluída.
    
VCSTATUS_DELETE_IS_MOVE 
  
> Quando excluídas, uma mensagem é movida para uma pasta de **Itens excluídos** no seu armazenamento de mensagens em vez de sendo imediatamente removido do seu armazenamento de mensagens. 
    
VCSTATUS_MOVE 
  
> A mensagem pode ser movida.
    
VCSTATUS_NEW_MESSAGE 
  
> Uma nova mensagem pode ser criada.
    
VCSTATUS_SAVE 
  
> A mensagem pode ser salva.
    
VCSTATUS_SUBMIT 
  
> A mensagem pode ser enviada.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Objetos de formulário chame o método **IMAPIMessageSite::GetSiteStatus** para obter os recursos do objeto de site a mensagem para a mensagem atual. Os sinalizadores retornados no parâmetro _lpulStatus_ fornecem informações sobre o site da mensagem. Normalmente, um formulário habilita ou desabilita o comandos de menu, dependendo de informações que os sinalizadores fornecem sobre os recursos da implementação do site de mensagem. Se uma nova mensagem for carregada para um formulário, o método [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) ou o método [IPersistMessage::Load](ipersistmessage-load.md) , os sinalizadores de status devem ser verificados. Alguns objetos de site de mensagem, especialmente objetos de somente leitura, não permitir que as mensagens sejam salvos ou excluído. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

O método **IMAPIMessageSite::GetSiteStatus** pode exigir o aplicativo cliente para realizar algumas cálculo para determinar quais operações podem ou não podem ser executadas na mensagem atual. Normalmente, o que envolve olhando a linha de status para o provedor de armazenamento de mensagem da mensagem atual, ou consultar o provedor de armazenamento para determinar quais ações o aplicativo cliente pode executar usando o armazenamento de mensagens. Por exemplo, para determinar se é necessário retornar o sinalizador MAPI_DELETE_IS_MOVE, verifique a mensagem repositório de propriedade do objeto **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) para ver se há uma pasta de **Itens excluídos** no armazenamento de mensagens. 
  
Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSiteStatus  <br/> |MFCMAPI usa o método **IMAPIMessageSite::GetSiteStatus** para obter o status do site especificado. Ele pode retornar VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE ou VCSTATUS_SUBMIT.  <br/> |
   
## <a name="see-also"></a>Confira também



[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[Propriedade canônica PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

