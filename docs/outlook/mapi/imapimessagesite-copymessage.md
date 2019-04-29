---
title: IMAPIMessageSiteCopyMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429997"
---
# <a name="imapimessagesitecopymessage"></a>IMAPIMessageSite::CopyMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia a mensagem atual para uma pasta.
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a>Parâmetros

 _pFolderDestination_
  
> no Um ponteiro para a pasta onde a mensagem deve ser copiada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_NO_SUPPORT 
  
> A operação não é suportada por este site de mensagem.
    
## <a name="remarks"></a>Comentários

Os objetos Form chamam o método **IMAPIMessageSite:: CopyMessage** para copiar a mensagem atual para uma nova pasta. **CopyMessage** não altera a mensagem que está sendo exibida para o usuário e nenhuma interface para a mensagem recém-criada é retornada ao formulário. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Uma implementação típica do método **CopyMessage** executa as seguintes tarefas: 
  
1. Cria uma nova mensagem para a mensagem atual a ser copiada.
    
2. Chama o método [IPersistMessage:: Save](ipersistmessage-save.md) com um ponteiro para a nova mensagem no parâmetro _PMessage_ e false no parâmetro _fSameAsLoad_ . 
    
3. Chama o método [IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) , passando NULL no parâmetro _PMessage_ . 
    
4. Chama o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) na nova mensagem. 
    
Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulários MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: CopyMessage  <br/> |Não implementado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

