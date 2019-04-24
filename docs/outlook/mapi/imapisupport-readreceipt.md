---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1915004847fdfd27c97656223866aaab9d3e59c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326303"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Gera um relatório de leitura ou não lido para uma mensagem.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o relatório de leitura ou não lido é gerado. O seguinte sinalizador pode ser definido:
    
MAPI_NON_READ 
  
> Um relatório não lido é gerado. Se MAPI_NON_READ não for definido, um relatório de leitura é gerado.
    
 _lpReadMessage_
  
> no Um ponteiro para a mensagem sobre a qual o relatório deve ser gerado.
    
 _lppEmptyMessage_
  
> [in, out] Na entrada, _lppEmptyMessage_ aponta para um ponteiro para uma mensagem vazia. Na saída, _lppEmptyMessage_ aponta para um ponteiro para a mensagem de relatório. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O relatório foi gerado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: ReadReceipt** é implementado apenas para objetos de suporte do provedor de repositório de mensagens. Os provedores de repositório de mensagens chamam o **ReadReceipt** para instruir o MAPI a gerar um relatório de leitura ou não leitura para a mensagem indicada pelo parâmetro _lpReadMessage_ . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **ReadReceipt** quando a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) estiver definida e uma das seguintes condições for verdadeira:
  
- A mensagem foi lida.
    
- A mensagem foi movida.
    
- A mensagem foi copiada.
    
- O método [IMessage:: SetReadFlag](imessage-setreadflag.md) da mensagem foi chamado. 
    
Não chama **ReadReceipt** quando uma mensagem é excluída. 
  
Um relatório de leitura ou de não leitura deve ser enviado apenas uma vez para uma mensagem. Acompanhar o status de leitura de uma mensagem e não enviar vários relatórios para uma única mensagem.
  
Se o parâmetro _lppEmptyMessage_ apontar para uma mensagem de relatório válida quando o MAPI retornar de **ReadReceipt**, chame o método [IMessage:: SubmitMessage](imessage-submitmessage.md) para enviar a mensagem e, em seguida, solte o ponteiro chamando seu **IUnknown: s: Release **método. 
  
Se o **ReadReceipt** falhar, a mensagem deverá ser liberada sem ser enviada. Se você armazenar o status de leitura da mensagem, poderá tentar gerar o relatório de leitura ou de não leitura mais tarde. 
  
Você pode ocultar ou exibir os relatórios de leitura e não leitura gerados por lojas em suas pastas. O armazenamento de relatórios de leitura e não leitura em pastas ocultas permite que você implemente segurança mais rígida.
  
## <a name="see-also"></a>Confira também



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[Propriedade canônica PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

