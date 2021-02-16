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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fa3f1d6339000fcc53e0ee22dafec4362e65ca7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309615"
---
# <a name="ipersistmessagesave"></a>IPersistMessage::Save

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Salva um formulário revisado de volta à mensagem a partir da qual ele foi carregado ou criado.
  
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
  
> [in] TRUE para indicar que a mensagem apontada por  _pMessage_ é a mensagem da qual o formulário foi carregado ou criado; caso contrário, FALSE. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O formulário foi salvo com êxito.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam o método **IPersistMessage::Save** para salvar um formulário revisado de volta à mensagem a partir da qual ele foi carregado ou criado. 
  
 **Save** só deve ser chamado quando o formulário estiver em seu [estado Normal.](normal-state.md) 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Não confirma as alterações salvas; fica ao chamador para confirma as alterações. Nunca faça alterações nas propriedades que pertencem à mensagem do formulário, exceto durante a **chamada Salvar.** 
  
Se  _fSameAsLoad_ for definido como TRUE, você poderá salvar as alterações na mensagem existente do formulário. Se  _fSameAsLoad_ for definido como FALSE, você deverá copiar todas as propriedades da mensagem original para a mensagem apontada por  _pMessage_ antes de executar o salvar. Use o método [IMAPIProp::CopyTo](imapiprop-copyto.md) da mensagem original para copiar as propriedades. 
  
Quando todas as propriedades foram copiadas, insira o [estado NoScribble.](noscribble-state.md) Se não ocorrerem erros, retorne S_OK. Caso contrário, retorne o erro da ação com falha. 
  
Se **Save** for chamado quando o formulário estiver em qualquer estado diferente de Normal, retorne E_UNEXPECTED. 
  
Para obter mais informações sobre como salvar objetos de armazenamento, consulte a documentação sobre os métodos [IPersistStorage.](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) 
  
## <a name="see-also"></a>Confira também



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Estados do formulário](form-states.md)

