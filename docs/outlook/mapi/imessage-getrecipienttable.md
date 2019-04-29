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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ca42e91528cdb7e61ae3620989c4a89966db1061
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424606"
---
# <a name="imessagegetrecipienttable"></a>IMessage::GetRecipientTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna a tabela de destinatários da mensagem.
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Bitmask dos sinalizadores que controlam o retorno da tabela. Os seguintes sinalizadores podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **** que GetRecipientTable seja retornado com êxito, possivelmente antes que a tabela esteja totalmente disponível para o cliente de chamada. Se a tabela não estiver disponível, fazer uma chamada subsequente para ela pode causar um erro. 
    
MAPI_UNICODE 
  
> As colunas de cadeia de caracteres devem estar no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres devem estar no formato ANSI.
    
 _lppTable_
  
> bota Ponteiro para um ponteiro para a tabela de destinatários.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela de destinatários foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMessage::** GetRecipientTable Retorna um ponteiro para a tabela de destinatários da mensagem, que inclui informações sobre todos os destinatários da mensagem. Há uma linha para cada destinatário. 
  
As tabelas de destinatários têm um conjunto de colunas diferente, dependendo se a mensagem foi enviada. Para obter uma lista completa das colunas em uma tabela de destinatários, consulte [tabelas de destinatários](recipient-tables.md).
  
Algumas tabelas de destinatários dão suporte a uma ampla variedade de restrições; outros não. O suporte para restrições depende da implementação do provedor de repositório de mensagens. 
  
Definir o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ afeta as seguintes chamadas para a tabela de destinatários: 
  
- [IMAPITable:: QueryColumns](imapitable-querycolumns.md) para recuperar o conjunto de colunas. 
    
- [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar linhas. 
    
- [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) para recuperar a ordem de classificação. 
    
Definir o sinalizador Unicode solicita que as informações de qualquer coluna de cadeia de caracteres retornada dessas chamadas estejam no formato Unicode. No enTanto, como nem todos os provedores de repositórios de mensagens dão suporte a Unicode, a configuração desse sinalizador é apenas uma solicitação.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode alterar uma tabela de destinatários enquanto ela estiver aberta chamando o método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) . O **ModifyRecipients** adiciona destinatários, exclui destinatários ou modifica as propriedades do destinatário. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)

