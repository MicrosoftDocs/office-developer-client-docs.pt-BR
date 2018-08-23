---
title: IMessageGetRecipientTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetRecipientTable
api_type:
- COM
ms.assetid: a335dfca-44da-452e-b16f-25d314b1758f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5908069f5fa887fd9d2e3f8c0df75f2e3d69515c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579533"
---
# <a name="imessagegetrecipienttable"></a>IMessage::GetRecipientTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna a tabela de destinatário da mensagem.
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Bitmask dos sinalizadores que controla o retorno da tabela. Sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **GetRecipientTable** retornar com êxito, possivelmente antes que a tabela é totalmente disponível para o cliente da chamada. Se a tabela não estiver disponível, fazendo uma chamada subsequente a ele pode causar um erro. 
    
MAPI_UNICODE 
  
> Colunas de cadeia de caracteres devem estar no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres devem estar no formato ANSI.
    
 _lppTable_
  
> [out] Ponteiro para um ponteiro para a tabela de destinatários.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A tabela de destinatários foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMessage::GetRecipientTable** retorna um ponteiro para a tabela de destinatário da mensagem, que inclui informações sobre todos os destinatários da mensagem. Não há uma linha para cada destinatário. 
  
Tabelas de destinatários têm outra coluna definir dependendo se a mensagem foi enviada. Para obter uma lista completa das colunas em uma tabela de destinatário, consulte [Tabelas do destinatário](recipient-tables.md).
  
Algumas tabelas destinatários oferecem suporte a uma ampla variedade de restrições; outros não. Suporte a restrições depende da implementação do provedor de repositório de mensagem. 
  
Definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ afeta as seguintes chamadas para a tabela de destinatários: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar o conjunto de coluna. 
    
- [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar linhas. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar a ordem de classificação. 
    
Definindo as solicitações de sinalizador Unicode que as informações de quaisquer colunas de cadeia de caracteres retornada dessas chamadas estar no formato Unicode. No entanto, porque nem todos os provedores de armazenamento de mensagem oferecem suporte a Unicode, defina esse sinalizador é apenas uma solicitação.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode alterar uma tabela de destinatário, enquanto ela está aberta chamando o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . **ModifyRecipients** adiciona destinatários, exclui destinatários ou modifica as propriedades do destinatário. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)

