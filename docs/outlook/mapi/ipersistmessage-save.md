---
title: IPersistMessageSave
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Save
api_type:
- COM
ms.assetid: 17875c13-f55b-4538-ac6f-c020281c3175
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: fa3f1d6339000fcc53e0ee22dafec4362e65ca7f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397153"
---
# <a name="ipersistmessagesave"></a>IPersistMessage::Save

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Salva um formulário revisado na mensagem do qual ele foi carregado ou criado.
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a>Parâmetros

 _pMessage_
  
> [in] Um ponteiro para a mensagem.
    
 _fSameAsLoad_
  
> [in] TRUE para indicar que a mensagem apontado por _pMessage_ é a mensagem a partir do qual o formulário foi carregado ou criado; Caso contrário, FALSE. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O formulário foi salvo com êxito.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método de **IPersistMessage::Save** para salvar um formulário revisado na mensagem do qual ele foi carregado ou criado. 
  
 **Salvar** só deve ser chamado quando o formulário está em seu estado [Normal](normal-state.md) . 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Não confirmar as alterações salvas; é até o chamador para confirmar as alterações. Nunca fazer alterações nas propriedades que pertencem a mensagem do formulário, exceto durante a chamada de **Salvar** . 
  
Se _fSameAsLoad_ for definido como TRUE, você pode salvar as alterações de mensagem existente do formulário. Se _fSameAsLoad_ estiver definida como FALSE, você deve copiar todas as propriedades da mensagem original na mensagem apontada pela _pMessage_ antes de salvar. Use o método de [IMAPIProp::CopyTo](imapiprop-copyto.md) da mensagem original para copiar as propriedades. 
  
Quando tiverem sido copiadas todas as propriedades, insira o estado de [NoScribble](noscribble-state.md) . Se nenhum erro ocorrer, retorne S_OK. Caso contrário, retornará o erro da ação com falha. 
  
Se **Salvar** é chamado quando o formulário estiver em qualquer estado que não seja Normal, retorne E_UNEXPECTED. 
  
Para obter mais informações sobre como salvar objetos de armazenamento, consulte a documentação sobre os métodos [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . 
  
## <a name="see-also"></a>Confira também



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Estados de formulários](form-states.md)

