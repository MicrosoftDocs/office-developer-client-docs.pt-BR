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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 87432d8982c5dc1f64396187739e97314edb385c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412881"
---
# <a name="imapiformmgrisinconflict"></a>IMAPIFormMgr::IsInConflict

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Determina se um formulário pode lidar com seus próprios conflitos de mensagem. Uma mensagem estará em conflito se tiver sido editada simultaneamente por mais de um usuário. Isso pode acontecer com mensagens em pastas públicas.
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Parâmetros

 _ulMessageFlags_
  
> no Um ponteiro para uma bitmask de sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uma mensagem que indica o estado atual da mensagem.
    
 _ulMessageStatus_
  
> no Uma bitmask de sinalizadores definidos pelo cliente ou definidos pelo provedor copiados da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) de uma mensagem que fornece informações adicionais sobre o estado da mensagem.
    
 _szMessageClass_
  
> no Uma cadeia de caracteres que nomeia a classe de mensagem da mensagem.
    
 _pFolderFocus_
  
> no Um ponteiro para a pasta que contém a mensagem. O parâmetro _pFolderFocus_ pode ser NULL se essa pasta não existir (por exemplo, se a mensagem estiver incorporada a outra mensagem). 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O formulário não manipula seus próprios conflitos de mensagem.
    
S_FALSE 
  
> O formulário manipula seus próprios conflitos de mensagem ou a mensagem para a qual as informações foram transmitidas não está em conflito.
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIFormMgr:: IsInConflict** para descobrir se um determinado formulário não manipula seus próprios conflitos de mensagem. **IsInConflict** verifica os bitmasks nos parâmetros _ulMessageFlags_ e _ulMessageStatus_ para a presença de um sinalizador de conflito. Se um sinalizador de conflito estiver definido, **IsInConflict** resolverá a classe de mensagem passada no parâmetro _SZMESSAGECLASS_ e retornará S_OK se o formulário não manipular seus próprios conflitos. **IsInConflict** retornará S_FALSE se o formulário manipular seus próprios conflitos. 
  
Um formulário que não manipula seus próprios conflitos deve ser aberto usando o método [IMAPIFormMgr:: loadform](imapiformmgr-loadform.md) e não pode reutilizar um objeto Form existente. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Os aplicativos clientes normalmente precisam lidar com conflitos quando os aplicativos são movidos de uma mensagem para a mensagem seguinte ou anterior em uma pasta. Se uma mensagem estiver em conflito, mas o servidor de formulário dessa mensagem puder lidar com conflitos, o aplicativo cliente deverá executar o código habitual para exibir a mensagem seguinte ou anterior. Se o servidor de formulário não puder lidar com conflitos, o aplicativo cliente deve continuar como se não estivesse ciente da classe de mensagem da mensagem seguinte ou anterior. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriedade canônica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

