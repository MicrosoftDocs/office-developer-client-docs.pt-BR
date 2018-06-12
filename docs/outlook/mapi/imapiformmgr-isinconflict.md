---
title: IMAPIFormMgrIsInConflict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgrIsInConflict
api_type:
- COM
ms.assetid: 5ca86ee8-1bf6-4ec8-95b3-575c22fbb170
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d8f28a6b0a1633b0060f02af7e38ef058527eb24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767042"
---
# <a name="imapiformmgrisinconflict"></a>IMAPIFormMgr::IsInConflict

  
  
**Aplica-se a**: Outlook 
  
Determina se um formulário pode lidar com conflitos sua própria mensagem. Uma mensagem está em conflito se ele tiver sido editado simultaneamente por mais de um usuário. Isso pode acontecer às mensagens em pastas públicas.
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Par�metros

 _ulMessageFlags_
  
> [in] Um ponteiro para uma bitmask dos sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uma mensagem que indica o estado atual da mensagem.
    
 _ulMessageStatus_
  
> [in] Uma bitmask dos sinalizadores definido pelo provedor ou cliente copiado da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) de uma mensagem que fornece informações adicionais sobre o estado da mensagem.
    
 _szMessageClass_
  
> [in] Uma cadeia de caracteres que nomeia a classe de mensagem da mensagem.
    
 _pFolderFocus_
  
> [in] Um ponteiro para a pasta que contém a mensagem. O parâmetro _pFolderFocus_ pode ser NULL se tal uma pasta não existir (por exemplo, se a mensagem é incorporada em outra mensagem). 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O formulário não lidar com conflitos sua própria mensagem.
    
S_FALSE 
  
> O formulário manipula conflitos sua própria mensagem ou a mensagem para os quais informações passadas não está em conflito.
    
## <a name="remarks"></a>Coment�rios

Visualizadores de formulário chame o método de **IMAPIFormMgr::IsInConflict** para descobrir se a determinado formulário não lidar com conflitos sua própria mensagem. **IsInConflict** verifica a bitmasks nos parâmetros _ulMessageFlags_ e _ulMessageStatus_ a presença de um sinalizador de conflito. Se for definido um sinalizador de conflito, **IsInConflict** resolva a classe de mensagem passada no parâmetro _szMessageClass_ e retorna S_OK se o formulário não manipular seus próprio conflitos. **IsInConflict** retorna S_FALSE se o formulário manipula o seus próprio conflitos. 
  
Um formulário que não lidar com seus próprio conflitos deve ser aberto usando o método [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) e não pode reutilizar um objeto de formulário existente. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Aplicativos clientes geralmente têm que lidar com conflitos quando os aplicativos se move de uma mensagem para a mensagem anterior ou seguinte em uma pasta. Se uma mensagem está em conflito, mas o servidor de formulário para essa mensagem pode lidar com conflitos, o aplicativo cliente deve executar o seu código usual para exibir a mensagem anterior ou seguinte. Se o servidor de formulário não pode lidar com conflitos, o aplicativo cliente deve continuar como se fosse não sabem da classe de mensagem da mensagem seguinte ou anterior. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[Propriedade canônico de PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriedade canônico de PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr: IUnknown](imapiformmgriunknown.md)

