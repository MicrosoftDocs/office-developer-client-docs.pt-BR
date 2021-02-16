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
  
Determina se um formulário pode lidar com seus próprios conflitos de mensagem. Uma mensagem está em conflito se tiver sido editada simultaneamente por mais de um usuário. Isso pode acontecer com mensagens em pastas públicas.
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Parâmetros

 _ulMessageFlags_
  
> [in] Um ponteiro para uma máscara de bits de sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uma mensagem que indica o estado atual da mensagem.
    
 _ulMessageStatus_
  
> [in] Uma bitmask de sinalizadores definidos pelo cliente ou definidos pelo provedor copiados da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) de uma mensagem que fornece informações adicionais sobre o estado da mensagem.
    
 _szMessageClass_
  
> [in] Uma cadeia de caracteres que nomeia a classe de mensagem da mensagem.
    
 _pFolderFocus_
  
> [in] Um ponteiro para a pasta que contém a mensagem. O  _parâmetro pFolderFocus_ poderá ser NULL se essa pasta não existir (por exemplo, se a mensagem estiver incorporada em outra mensagem). 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O formulário não trata seus próprios conflitos de mensagem.
    
S_FALSE 
  
> O formulário lida com seus próprios conflitos de mensagem ou a mensagem para a qual as informações foram passadas não está em conflito.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam o método **IMAPIFormMgr::IsInConflict** para descobrir se um formulário específico não trata seus próprios conflitos de mensagem. **IsInConflict** verifica as bitmasks nos parâmetros  _ulMessageFlags_ e  _ulMessageStatus_ para a presença de um sinalizador de conflito. Se um sinalizador de conflito for definido, **IsInConflict** resolverá a classe de mensagem passada no parâmetro  _szMessageClass_ e retornará S_OK se o formulário não manipular seus próprios conflitos. **IsInConflict** retornará S_FALSE se o formulário tratar seus próprios conflitos. 
  
Um formulário que não trata seus próprios conflitos deve ser aberto usando o método [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) e não pode reutilizar um objeto de formulário existente. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Os aplicativos cliente geralmente têm que lidar com conflitos quando os aplicativos se movem de uma mensagem para a próxima ou a mensagem anterior em uma pasta. Se uma mensagem estiver em conflito, mas o servidor de formulário para essa mensagem puder lidar com conflitos, o aplicativo cliente deverá executar seu código usual para exibir a mensagem seguinte ou anterior. Se o servidor de formulário não puder lidar com conflitos, o aplicativo cliente deverá continuar como se não tivesse conhecimento da classe de mensagem da mensagem seguinte ou anterior. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriedade canônica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

