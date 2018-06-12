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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 7062e0b73d2d70be12fb9cead6813ef9c36fdd43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767093"
---
# <a name="imapimessagesitenewmessage"></a>IMAPIMessageSite::NewMessage

  
  
**Aplica-se a**: Outlook 
  
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

## <a name="parameters"></a>Par�metros

 _fComposeInFolder_
  
> [in] Indica a mensagem na pasta na qual deve ser composta. Se a variável for FALSE, o parâmetro _pFolderFocus_ será ignorado e a tela de formulário pode escreva a mensagem em qualquer pasta. Se a variável é TRUE e NULL é passada no parâmetro _pFolderFocus_ , a mensagem é composta na pasta atual. Se a variável for TRUE e um valor de não-nulo é transmitido em _pFolderFocus_, a mensagem é composta na pasta indicada por _pFolderFocus_.
    
 _pFolderFocus_
  
> [in] Um ponteiro para a pasta onde a nova mensagem é criada.
    
 _pPersistMessage_
  
> [in] Um ponteiro para o objeto de formulário para o novo formulário.
    
 _ppMessage_
  
> [out] Um ponteiro para um ponteiro para a nova mensagem.
    
 _ppMessageSite_
  
> [out] Um ponteiro para um ponteiro para um objeto de site de mensagem da nova mensagem.
    
 _ppViewContext_
  
> [out] Um ponteiro para um ponteiro para um contexto de modo de exibição que é apropriado para passagem para um novo formulário com a nova mensagem. Se o formulário implementa seu próprio contexto de modo de exibição, NULL pode ser passado no parâmetro _ppViewContext_ . 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Coment�rios

Objetos de formulário chame o método **IMAPIMessageSite::NewMessage** para criar uma nova mensagem. O formulário usa **NewMessage** para fazer uma nova mensagem e o site de mensagem associada a partir de seu modo de exibição. Em seguida, ele pode modificar a nova mensagem. 
  
Você também pode obter um contexto de modo de exibição associado, passando um valor nulo no parâmetro _ppViewContext_ . Nesse contexto de modo de exibição pode ser usado diretamente, ou podem ser agregado e passado para a nova mensagem. Se uma implementação completa for necessária, passe NULL no _ppViewContext_.
  
Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::NewMessage  <br/> |MFCMAPI usa o método **IMAPIMessageSite::NewMessage** para criar uma nova mensagem, instanciar um novo Visualizador de formulário e chamar **SetPersist** para definir a mensagem no Visualizador do formulário. Finalmente, ela retornará o Visualizador do formulário como o site da mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

