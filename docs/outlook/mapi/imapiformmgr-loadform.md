---
title: IMAPIFormMgrLoadForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.LoadForm
api_type:
- COM
ms.assetid: 5ca500c3-c737-45a5-b0fc-473b75c1d68d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7e445646477ad1fc56b41141b541358d9b9f9616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418782"
---
# <a name="imapiformmgrloadform"></a>IMAPIFormMgr::LoadForm

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicia um formulário para abrir uma mensagem existente.
  
```cpp
HRESULT LoadForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pmsg,
  LPMAPIVIEWCONTEXT pViewContext,
  REFIID riid,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um alça para a janela pai do indicador de progresso que é exibido enquanto o formulário é aberto. O _parâmetro ulUIParam é_ ignorado, a menos que o MAPI_DIALOG padrão seja definido no parâmetro _ulFlags._ 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o formulário é aberto. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DIALOG 
  
> Exibe uma interface do usuário para fornecer status ou solicitar ao usuário mais informações. Se esse sinalizador não estiver definido, nenhuma interface do usuário será exibida.
    
MAPIFORM_EXACTMATCH 
  
> Somente cadeias de caracteres de classe de mensagem que sejam uma combinação exata devem ser resolvidas.
    
 _lpszMessageClass_
  
> [in] Um ponteiro para uma cadeia de caracteres que nomeia a classe de mensagem da mensagem a ser carregada. Se NULL for passado no parâmetro _lpszMessageClass,_ a classe de mensagem será determinada a partir da mensagem apontada pelo _parâmetro pmsg._ 
    
 _ulMessageStatus_
  
> [in] Uma bitmask de sinalizadores definidos pelo cliente ou definidos pelo provedor copiados da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem que fornece informações sobre o estado da mensagem. O  _parâmetro ulMessageStatus_ deve ser definido se  _lpszMessageClass_ for non-NULL; caso contrário,  _ulMessageStatus_ será ignorado. 
    
 _ulMessageFlags_
  
> [in] Um ponteiro para uma máscara de bits de sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem que indica o estado atual da mensagem. O  _parâmetro ulMessageFlags_ deve ser definido se  _lpszMessageClass_ for non-NULL; caso contrário,  _ulMessageFlags_ será ignorado. 
    
 _pFolderFocus_
  
> [in] Um ponteiro para a pasta que contém diretamente a mensagem. O  _parâmetro pFolderFocus_ poderá ser NULL se essa pasta não existir (por exemplo, se a mensagem estiver incorporada em outra mensagem). 
    
 _pMessageSite_
  
> [in] Um ponteiro para o site de mensagens da mensagem.
    
 _pmsg_
  
> [in] Um ponteiro para a mensagem.
    
 _pViewContext_
  
> [in] Um ponteiro para o contexto de exibição da mensagem. O  _parâmetro pViewContext_ pode ser NULL. 
    
 _riid_
  
> [in] O IID (identificador de interface) da interface a ser usada para o objeto de formulário retornado. O  _parâmetro riid_ não deve ser NULL. 
    
 _ppvObj_
  
> [out] Um ponteiro para um ponteiro para a interface retornada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_NO_INTERFACE 
  
> O formulário não dá suporte à interface solicitada.
    
MAPI_E_NOT_FOUND 
  
> A classe de mensagem passada  _em lpszMessageClass_ não combina com a classe de mensagem de nenhum formulário na biblioteca de formulário. 
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam **o método IMAPIFormMgr::LoadForm** para abrir um formulário para uma mensagem existente. **LoadForm** abre o objeto de formulário, carrega a mensagem no objeto de formulário, configura o contexto de exibição apropriado, se necessário, e retorna a interface solicitada para o objeto de formulário. 
  
O  _parâmetro pFolderFocus_ aponta para a pasta que contém a mensagem. Se a mensagem estiver incorporada em outra mensagem,  _pFolderFocus_ deverá ser NULL. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se NULL for passado em  _lpszMessageClass_, a implementação obterá a classe de mensagem, o status e os sinalizadores da mensagem das propriedades **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** e **PR_MESSAGE_FLAGS** da mensagem. Se uma cadeia de caracteres de classe de mensagem for fornecida em  _lpszMessageClass_, a implementação deverá usar os valores em  _ulMessageStatus_ e  _ulMessageFlags_.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI usa o **método IMAPIFormMgr::LoadForm** para carregar um formulário antes de exibi-lo.  <br/> |
   
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagMessageClass](pidtagmessageclass-canonical-property.md)
  
[Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriedade canônica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

