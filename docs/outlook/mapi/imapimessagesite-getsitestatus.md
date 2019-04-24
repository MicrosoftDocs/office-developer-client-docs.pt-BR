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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355808"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna informações de um objeto de site de mensagem sobre os recursos do site da mensagem para a mensagem atual.
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parâmetros

 _lpulStatus_
  
> bota Um ponteiro para uma bitmask de sinalizadores que fornece informações sobre o status da mensagem. Os seguintes sinalizadores podem ser definidos:
    
VCSTATUS_COPY 
  
> A mensagem pode ser copiada. 
    
VCSTATUS_DELETE 
  
> A mensagem pode ser excluída.
    
VCSTATUS_DELETE_IS_MOVE 
  
> Quando excluído, uma mensagem é movida para uma pasta **itens excluídos** em seu repositório de mensagens, em vez de ser imediatamente removida do seu repositório de mensagens. 
    
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
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Os objetos Form chamam o método **IMAPIMessageSite:: GetSiteStatus** para obter os recursos do objeto site da mensagem para a mensagem atual. Os sinalizadores retornados no parâmetro _lpulStatus_ fornecem informações sobre o site da mensagem. Normalmente, um formulário habilita ou desabilita comandos de menu, dependendo das informações que os sinalizadores fornecem sobre os recursos da implementação do site da mensagem. Se uma nova mensagem é carregada em um formulário pelo método [IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) ou o método [IPersistMessage:: Load](ipersistmessage-load.md) , os sinalizadores de status devem ser verificados. Alguns objetos do site de mensagens, especialmente objetos somente leitura, não permitem que as mensagens sejam salvas ou excluídas. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

O método **IMAPIMessageSite:: GetSiteStatus** pode exigir que o aplicativo cliente faça alguns cálculos para determinar quais operações podem ou não ser realizadas na mensagem atual. Normalmente, isso envolve a análise da linha de status do provedor de repositório de mensagens da mensagem atual ou a consulta do provedor de repositório para determinar quais ações o aplicativo cliente pode executar usando o repositório de mensagens. Por exemplo, para determinar se o sinalizador MAPI_DELETE_IS_MOVE deve ser retornado, verifique a propriedade **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) do objeto do repositório de mensagens para ver se há uma pasta **itens excluídos** no repositório de mensagens. 
  
Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulário MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: GetSiteStatus  <br/> |MFCMAPI usa o método **IMAPIMessageSite:: GetSiteStatus** para obter o status do site especificado. Pode retornar VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE ou VCSTATUS_SUBMIT.  <br/> |
   
## <a name="see-also"></a>Confira também



[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[Propriedade canônica PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

