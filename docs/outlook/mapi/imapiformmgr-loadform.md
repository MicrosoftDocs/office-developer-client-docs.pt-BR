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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321685"
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
  
> no Uma alça para a janela pai do indicador de progresso exibida enquanto o formulário é aberto. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MAPI_DIALOG esteja definido no parâmetro _parâmetroulflags_ . 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o formulário é aberto. Os seguintes sinalizadores podem ser definidos:
    
MAPI_DIALOG 
  
> Exibe uma interface do usuário para fornecer status ou solicitar mais informações ao usuário. Se esse sinalizador não for definido, nenhuma interface de usuário será exibida.
    
MAPIFORM_EXACTMATCH 
  
> Somente as cadeias de caracteres de classe de mensagem que têm uma correspondência exata devem ser resolvidas.
    
 _lpszMessageClass_
  
> no Um ponteiro para uma cadeia de caracteres que nomeia a classe da mensagem a ser carregada. Se NULL for passado no parâmetro _lpszMessageClass_ , a classe Message será determinada da mensagem indicada pelo parâmetro _pMsg_ . 
    
 _ulMessageStatus_
  
> no Uma bitmask de sinalizadores definidos pelo cliente ou definidos pelo provedor copiados da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem que fornece informações sobre o estado da mensagem. O parâmetro _ulMessageStatus_ deve ser definido se _LPSZMESSAGECLASS_ for não nulo; caso contrário, _ulMessageStatus_ será ignorada. 
    
 _ulMessageFlags_
  
> no Um ponteiro para uma bitmask de sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem que indica o estado atual da mensagem. O parâmetro _ulMessageFlags_ deve ser definido se _LPSZMESSAGECLASS_ for não nulo; caso contrário, _ulMessageFlags_ será ignorada. 
    
 _pFolderFocus_
  
> no Um ponteiro para a pasta que contém diretamente a mensagem. O parâmetro _pFolderFocus_ pode ser NULL se essa pasta não existir (por exemplo, se a mensagem estiver incorporada a outra mensagem). 
    
 _pMessageSite_
  
> no Um ponteiro para o site de mensagens da mensagem.
    
 _pMsg_
  
> no Um ponteiro para a mensagem.
    
 _pViewContext_
  
> no Um ponteiro para o contexto de exibição da mensagem. O parâmetro _pViewContext_ pode ser NULL. 
    
 _riid_
  
> no O identificador de interface (IID) da interface a ser usado para o objeto Form retornado. O parâmetro _riid_ não deve ser nulo. 
    
 _ppvObj_
  
> bota Um ponteiro para um ponteiro para a interface retornada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_NO_INTERFACE 
  
> O formulário não dá suporte à interface solicitada.
    
MAPI_E_NOT_FOUND 
  
> A classe de mensagens passada no _lpszMessageClass_ não corresponde à classe da mensagem de qualquer formulário na biblioteca de formulários. 
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIFormMgr:: loadform** para abrir um formulário para uma mensagem existente. **Loadform** abre o objeto Form, carrega a mensagem no objeto Form, configura o contexto de exibição apropriado, se necessário, e retorna a interface solicitada para o objeto Form. 
  
O parâmetro _pFolderFocus_ aponta para a pasta que contém a mensagem. Se a mensagem for incorporada a outra mensagem, _pFolderFocus_ deverá ser NULL. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se NULL for passado no _lpszMessageClass_, a implementação obterá a classe de mensagem, o status e os sinalizadores da mensagem de **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** e **PR_MESSAGE_FLAGS **Propriedades. Se uma cadeia de caracteres de classe de mensagem for fornecida no _lpszMessageClass_, a implementação deverá usar os valores em _ulMessageStatus_ e _ulMessageFlags_.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI usa o método **IMAPIFormMgr:: loadform** para carregar um formulário antes de exibi-lo.  <br/> |
   
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagMessageClass](pidtagmessageclass-canonical-property.md)
  
[Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriedade canônica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

