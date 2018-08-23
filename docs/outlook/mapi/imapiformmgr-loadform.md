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
ms.openlocfilehash: 3e758acfa1cf0c11be666dd730d9bf589d2e9d77
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586211"
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
  
> [in] Um identificador para a janela pai do indicador de progresso é exibida enquanto o formulário é aberto. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MAPI_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o formulário é aberto. Sinalizadores a seguir podem ser definidos:
    
MAPI_DIALOG 
  
> Exibe uma interface de usuário para fornecer status ou solicita ao usuário para obter mais informações. Se esse sinalizador não estiver definida, nenhuma interface de usuário é exibida.
    
MAPIFORM_EXACTMATCH 
  
> Apenas mensagem classe cadeias de caracteres que são uma correspondência exata devem ser resolvidas.
    
 _lpszMessageClass_
  
> [in] Um ponteiro para uma cadeia de caracteres que nomeia a classe de mensagem da mensagem a ser carregada. Se o parâmetro _lpszMessageClass_ é passado NULL, a classe da mensagem é determinada da mensagem apontada pelo parâmetro _pmsg_ . 
    
 _ulMessageStatus_
  
> [in] Uma bitmask dos sinalizadores definido pelo provedor ou cliente copiado da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem, que fornece informações sobre o estado da mensagem. O parâmetro _ulMessageStatus_ deve ser definido se _lpszMessageClass_ for não-nulo; Caso contrário, _ulMessageStatus_ será ignorada. 
    
 _ulMessageFlags_
  
> [in] Um ponteiro para uma bitmask dos sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem que indica o estado atual da mensagem. O parâmetro _ulMessageFlags_ deve ser definido se _lpszMessageClass_ for não-nulo; Caso contrário, _ulMessageFlags_ será ignorada. 
    
 _pFolderFocus_
  
> [in] Um ponteiro para a pasta que contém diretamente a mensagem. O parâmetro _pFolderFocus_ pode ser NULL se tal uma pasta não existir (por exemplo, se a mensagem é incorporada em outra mensagem). 
    
 _pMessageSite_
  
> [in] Um ponteiro para o site de mensagem da mensagem.
    
 _pmsg_
  
> [in] Um ponteiro para a mensagem.
    
 _pViewContext_
  
> [in] Um ponteiro para o contexto de modo de exibição para a mensagem. O parâmetro _pViewContext_ pode ser NULL. 
    
 _riid_
  
> [in] O identificador de interface (IID) da interface a ser usado para o objeto de formulário retornado. O parâmetro _riid_ não deve ser NULL. 
    
 _ppvObj_
  
> [out] Um ponteiro para um ponteiro para a interface retornada.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_NO_INTERFACE 
  
> O formulário não suporta a interface solicitada.
    
E_NOT_FOUND 
  
> A classe de mensagem passada _lpszMessageClass_ não coincide com a classe de mensagem para qualquer formulário na biblioteca de formulários. 
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método de **IMAPIFormMgr::LoadForm** para abrir um formulário para uma mensagem existente. **LoadForm** abre o objeto de formulário, carrega a mensagem para o objeto form, configura o contexto de modo de exibição apropriado, se necessário e retorna a interface solicitada para o objeto de formulário. 
  
O parâmetro _pFolderFocus_ aponta para a pasta que contém a mensagem. Se a mensagem está incorporada em outra mensagem, _pFolderFocus_ deve ser NULL. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Se NULL for passado _lpszMessageClass_, a implementação obtém a classe de mensagem da mensagem, status e sinalizadores do **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) da mensagem, **PR_MSG_STATUS** e **PR_MESSAGE_FLAGS **propriedades. Se uma cadeia de caracteres de classe de mensagem é fornecida em _lpszMessageClass_, a implementação deve usar os valores em _ulMessageStatus_ e _ulMessageFlags_.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI usa o método **IMAPIFormMgr::LoadForm** para carregar um formulário antes de exibi-lo.  <br/> |
   
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagMessageClass](pidtagmessageclass-canonical-property.md)
  
[Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriedade canônica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

