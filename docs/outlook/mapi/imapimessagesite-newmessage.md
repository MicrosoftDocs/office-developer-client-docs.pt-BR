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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321452"
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
  
> no Indica em qual pasta a mensagem deve ser redigida. Se a variável for FALSE, o parâmetro _pFolderFocus_ será ignorado e o Visualizador de formulários poderá redigir a mensagem em qualquer pasta. Se a variável for TRUE e NULL for passado no parâmetro _pFolderFocus_ , a mensagem será composta na pasta atual. Se a variável for TRUE e um valor não nulo for passado em _pFolderFocus_, a mensagem será composta na pasta indicada por _pFolderFocus_.
    
 _pFolderFocus_
  
> no Um ponteiro para a pasta onde a nova mensagem é criada.
    
 _pPersistMessage_
  
> no Um ponteiro para o objeto Form para o novo formulário.
    
 _ppMessage_
  
> bota Um ponteiro para um ponteiro para a nova mensagem.
    
 _ppMessageSite_
  
> bota Um ponteiro para um ponteiro para um objeto de site de mensagem para a nova mensagem.
    
 _ppViewContext_
  
> bota Um ponteiro para um ponteiro para um contexto de exibição que é apropriado para passar para um novo formulário com a nova mensagem. Se o formulário implementar seu próprio contexto de exibição, NULL pode ser passado no parâmetro _ppViewContext_ . 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Os objetos Form chamam o método **IMAPIMessageSite:: NewMessage** para criar uma nova mensagem. O formulário usa **NewMessage** para obter uma nova mensagem e o site de mensagem associado de seu modo de exibição. Em seguida, ele pode modificar a nova mensagem. 
  
Você também pode obter um contexto de exibição associado passando um valor não nulo no parâmetro _ppViewContext_ . Este contexto de exibição pode ser usado diretamente ou pode ser agregado e transmitido para a nova mensagem. Se for necessária uma implementação completa, passe NULL no _ppViewContext_.
  
Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulário MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: NewMessage  <br/> |MFCMAPI usa o método **IMAPIMessageSite:: NewMessage** para criar uma nova mensagem, criar uma instância de um novo Visualizador de **** formulários e chamar setpersist para definir a mensagem no Visualizador de formulários. Por fim, ele retorna o Visualizador de formulários como o site de mensagens.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

