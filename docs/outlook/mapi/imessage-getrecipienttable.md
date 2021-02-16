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
  
> [in] Máscara de bits de sinalizadores que controla o retorno da tabela. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **GetRecipientTable** retorne com êxito, possivelmente antes que a tabela fique totalmente disponível para o cliente de chamada. Se a tabela não estiver disponível, fazer uma chamada subsequente pode causar um erro. 
    
MAPI_UNICODE 
  
> As colunas de cadeia de caracteres devem estar no formato Unicode. Se o MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres deverão estar no formato ANSI.
    
 _lppTable_
  
> [out] Ponteiro para um ponteiro para a tabela de destinatários.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela de destinatários foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMessage::GetRecipientTable** retorna um ponteiro para a tabela de destinatários da mensagem, que inclui informações sobre todos os destinatários da mensagem. Há uma linha para cada destinatário. 
  
As tabelas de destinatários têm um conjunto de colunas diferente, dependendo se a mensagem foi enviada. Para uma lista completa das colunas em uma tabela de destinatários, consulte [Tabelas de Destinatários.](recipient-tables.md)
  
Algumas tabelas de destinatários suportam uma ampla variedade de restrições; outras não fazem isso. O suporte para restrições depende da implementação do provedor do armazenamento de mensagens. 
  
A definição MAPI_UNICODE sinalizador de configuração no  _parâmetro ulFlags_ afeta as seguintes chamadas para a tabela de destinatários: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar o conjunto de colunas. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar linhas. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar a ordem de classificação. 
    
A configuração do sinalizador Unicode solicita que as informações de quaisquer colunas de cadeia de caracteres retornadas dessas chamadas sejam no formato Unicode. No entanto, como nem todos os provedores de armazenamento de mensagens suportam Unicode, definir esse sinalizador é apenas uma solicitação.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode alterar uma tabela de destinatário enquanto ela estiver aberta chamando o [método IMessage::ModifyRecipients.](imessage-modifyrecipients.md) **ModifyRecipients** adiciona destinatários, exclui destinatários ou modifica propriedades de destinatário. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)

