---
title: IMAPIMessageSiteNewMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.NewMessage
api_type:
- COM
ms.assetid: ce6b6e6c-7f22-43c2-8182-90cf6db93844
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f51dd1fe533d0577996e6e1be185302f2dc972fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438768"
---
# <a name="imapimessagesitenewmessage"></a>IMAPIMessageSite::NewMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma nova mensagem.
  
```cpp
HRESULT NewMessage(
  ULONG fComposeInFolder,
  LPMAPIFOLDER pFolderFocus,
  LPPERSISTMESSAGE pPersistMessage,
  LPMESSAGE FAR * ppMessage,
  LPMAPIMESSAGESITE FAR * ppMessageSite,
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Parâmetros

 _fComposeInFolder_
  
> [in] Indica em qual pasta a mensagem deve ser composta. Se a variável for FALSE, o parâmetro  _pFolderFocus_ será ignorado e o visualizador de formulário poderá compor a mensagem em qualquer pasta. Se a variável for TRUE e NULL for passada no parâmetro  _pFolderFocus,_ a mensagem será composta na pasta atual. Se a variável for TRUE e um valor não NULO for passado em  _pFolderFocus_, a mensagem será composta na pasta apontada por  _pFolderFocus_.
    
 _pFolderFocus_
  
> [in] Um ponteiro para a pasta onde a nova mensagem é criada.
    
 _pPersistMessage_
  
> [in] Um ponteiro para o objeto de formulário para o novo formulário.
    
 _ppMessage_
  
> [out] Um ponteiro para um ponteiro para a nova mensagem.
    
 _ppMessageSite_
  
> [out] Um ponteiro para um ponteiro para um objeto de site de mensagem para a nova mensagem.
    
 _ppViewContext_
  
> [out] Um ponteiro para um ponteiro para um contexto de exibição apropriado para passar para um novo formulário com a nova mensagem. Se o formulário implementa seu próprio contexto de exibição, NULL pode ser passado no _parâmetro ppViewContext._ 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Os objetos de formulário chamam **o método IMAPIMessageSite::NewMessage** para criar uma nova mensagem. O formulário usa **NewMessage** para obter uma nova mensagem e o site de mensagens associado de sua exibição. Em seguida, ele pode modificar a nova mensagem. 
  
Você também pode obter um contexto de exibição associado passando um valor não NULO no _parâmetro ppViewContext._ Esse contexto de exibição pode ser usado diretamente ou pode ser agregado e passado para a nova mensagem. Se uma implementação completa for necessária, passe NULL em  _ppViewContext_.
  
Para uma lista de interfaces relacionadas a servidores de formulário, consulte [MAPI Form Interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::NewMessage  <br/> |MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer. Finalmente, ele retorna o visualizador de formulário como o site de mensagens.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

