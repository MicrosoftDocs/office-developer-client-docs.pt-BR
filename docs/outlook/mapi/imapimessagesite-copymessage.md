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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 5bf2ff74f6cda01608efd4b372aa4b03468c820f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767073"
---
# <a name="imapimessagesitecopymessage"></a>IMAPIMessageSite::CopyMessage

  
  
**Aplica-se a**: Outlook 
  
Copia a mensagem atual para uma pasta.
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a>Par�metros

 _pFolderDestination_
  
> [in] Um ponteiro para a pasta onde a mensagem deve ser copiado.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_NO_SUPPORT 
  
> A operação não é suportada por este site de mensagem.
    
## <a name="remarks"></a>Coment�rios

Objetos de formulário chame o método **IMAPIMessageSite::CopyMessage** para copiar a mensagem atual para uma nova pasta. **CopyMessage** não altera a mensagem atualmente estiver sendo exibida ao usuário e nenhuma interface para a mensagem recém-criado é retornado ao formulário. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Uma implementação típica do método **CopyMessage** executa as seguintes tarefas: 
  
1. Cria uma nova mensagem para a mensagem atual deve ser copiado para.
    
2. Chama o método [IPersistMessage::Save](ipersistmessage-save.md) com um ponteiro para a nova mensagem no parâmetro _pMessage_ e FALSE no parâmetro _fSameAsLoad_ . 
    
3. Chama o método [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) , passando NULL no parâmetro _pMessage_ . 
    
4. Chama o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) na nova mensagem. 
    
Para obter uma lista das interfaces que estão relacionados aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CopyMessage  <br/> |Não foi implementado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

