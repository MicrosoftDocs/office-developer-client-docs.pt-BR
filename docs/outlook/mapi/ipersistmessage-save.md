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
  
Salva um formulário revisado de volta para a mensagem a partir da qual foi carregado ou criado.
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a>Parâmetros

 _pMessage_
  
> no Um ponteiro para a mensagem.
    
 _fSameAsLoad_
  
> no TRUE para indicar que a mensagem indicada por _PMessage_ é a mensagem a partir da qual o formulário foi carregado ou criado; caso contrário, FALSE. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O formulário foi salvo com êxito.
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IPersistMessage:: Save** para salvar um formulário revisado de volta para a mensagem a partir da qual foi carregado ou criado. 
  
 **Save** só deve ser chamado quando o formulário estiver em seu estado [normal](normal-state.md) . 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Não confirmar as alterações salvas; o chamador deve confirmar as alterações. Nunca faça alterações nas propriedades que pertencem à mensagem do formulário, exceto durante a chamada de **salvamento** . 
  
Se _fSameAsLoad_ estiver definido como true, você poderá salvar as alterações na mensagem existente do formulário. Se _fSameAsLoad_ estiver definido como false, você deverá copiar todas as propriedades da mensagem original para a mensagem indicada por _PMessage_ antes de executar Save. Use o método [IMAPIProp:: CopyTo](imapiprop-copyto.md) da mensagem original para copiar as propriedades. 
  
Quando todas as propriedades tiverem sido copiadas, insira [](noscribble-state.md) o estado norabisco. Se nenhum erro ocorrer, retorne S_OK. Caso contrário, retorne o erro da ação com falha. 
  
Se **Save** for chamado quando o formulário estiver em qualquer estado diferente de normal, retornar E_UNEXPECTED. 
  
Para obter mais informações sobre como salvar objetos de armazenamento, consulte a documentação nos métodos [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . 
  
## <a name="see-also"></a>Confira também



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Estados de formulário](form-states.md)

