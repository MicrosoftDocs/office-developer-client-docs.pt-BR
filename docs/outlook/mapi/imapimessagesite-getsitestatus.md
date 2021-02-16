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
ms.openlocfilehash: ab4a06a20c71943f9b649d8f22377f59223e9717
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430123"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna informações de um objeto de site de mensagem sobre os recursos do site de mensagens para a mensagem atual.
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parâmetros

 _lpulStatus_
  
> [out] Um ponteiro para uma máscara de bits de sinalizadores que fornece informações sobre o status da mensagem. Os sinalizadores a seguir podem ser definidos:
    
VCSTATUS_COPY 
  
> A mensagem pode ser copiada. 
    
VCSTATUS_DELETE 
  
> A mensagem pode ser excluída.
    
VCSTATUS_DELETE_IS_MOVE 
  
> Quando excluída, uma mensagem é movida para **uma** pasta Itens Excluídos em seu armazenamento de mensagens, em vez de ser removida imediatamente do seu armazenamento de mensagens. 
    
VCSTATUS_MOVE 
  
> A mensagem pode ser movida.
    
VCSTATUS_NEW_MESSAGE 
  
> Uma nova mensagem pode ser criada.
    
VCSTATUS_SAVE 
  
> A mensagem pode ser salva.
    
VCSTATUS_SUBMIT 
  
> A mensagem pode ser enviada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Os objetos de formulário chamam o método **IMAPIMessageSite::GetSiteStatus** para obter os recursos do objeto de site de mensagens para a mensagem atual. Os sinalizadores retornados no parâmetro  _lpulStatus_ fornecem informações sobre o site de mensagens. Normalmente, um formulário habilita ou desabilita comandos de menu, dependendo das informações que os sinalizadores fornecem sobre os recursos da implementação do site de mensagens. Se uma nova mensagem for carregada em um formulário pelo método [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) ou pelo método [IPersistMessage::Load,](ipersistmessage-load.md) os sinalizadores de status deverão ser verificados. Alguns objetos de site de mensagens, especialmente objetos somente leitura, não permitem que as mensagens sejam salvas ou excluídas. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

O **método IMAPIMessageSite::GetSiteStatus** pode exigir que o aplicativo cliente faça algum cálculo para determinar quais operações podem ou não ser executadas na mensagem atual. Normalmente, isso envolve consultar a linha de status do provedor de armazenamento de mensagens da mensagem atual ou consultar o provedor do armazenamento para determinar quais ações o aplicativo cliente pode executar usando o armazenamento de mensagens. Por exemplo, para determinar se é preciso retornar o sinalizador MAPI_DELETE_IS_MOVE, verifique **a** propriedade **PR_IPM_WASTEBASKET_ENTRYID** do objeto de armazenamento de mensagens ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) para ver se há uma pasta Itens Excluídos no armazenamento de mensagens. 
  
Para uma lista de interfaces relacionadas a servidores de formulário, consulte [MAPI Form Interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSiteStatus  <br/> |MFCMAPI usa o **método IMAPIMessageSite::GetSiteStatus** para obter o status do site especificado. Ele pode retornar VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE ou VCSTATUS_SUBMIT.  <br/> |
   
## <a name="see-also"></a>Confira também



[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[Propriedade canônica PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

