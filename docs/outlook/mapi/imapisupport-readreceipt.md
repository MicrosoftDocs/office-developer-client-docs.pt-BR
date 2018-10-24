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
ms.openlocfilehash: e785d42639d51dab154a0bde239f858a92ddd143
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588619"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Gera uma leitura ou relatório nonread para uma mensagem.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o leitura ou nonread relatório é gerado. O seguinte sinalizador pode ser definido:
    
MAPI_NON_READ 
  
> É gerado um relatório de nonread. Se MAPI_NON_READ não estiver definida, é gerado um relatório de leitura.
    
 _lpReadMessage_
  
> [in] Um ponteiro para a mensagem sobre o qual o relatório deve ser gerado.
    
 _lppEmptyMessage_
  
> [além, out] Na entrada, _lppEmptyMessage_ aponta para um ponteiro para uma mensagem vazia. Na saída, _lppEmptyMessage_ aponta para um ponteiro para a mensagem de relatório. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O relatório foi gerado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::ReadReceipt** é implementado apenas para objetos de suporte do provedor de repositório de mensagem. Provedores de armazenamento de mensagem chamarem **ReadReceipt** para instruir o MAPI para gerar uma leitura ou relatório nonread da mensagem apontado pelo parâmetro _lpReadMessage_ . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **ReadReceipt** quando a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) estiver definida e uma das seguintes condições for verdadeira:
  
- A mensagem foi lido.
    
- A mensagem foi movida.
    
- A mensagem foi copiada.
    
- Método de [IMessage::SetReadFlag](imessage-setreadflag.md) da mensagem foi chamado. 
    
Não chame **ReadReceipt** quando uma mensagem é excluída. 
  
Uma leitura ou relatório nonread deverão ser enviado apenas uma vez para uma mensagem. Manter um registro de status de leitura da mensagem e não envie vários relatórios de uma única mensagem.
  
Se o parâmetro _lppEmptyMessage_ aponta para uma mensagem de relatório válido quando MAPI retorna da **ReadReceipt**, chame o método de [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar a mensagem e solte o ponteiro chamando seu **IUnknown:s:Release **método. 
  
Se **ReadReceipt** falhar, a mensagem deve ser liberada sem ser enviada. Se você armazenar status de leitura da mensagem, você pode tentar gerar o relatório nonread ou leitura mais tarde. 
  
Você pode ocultar ou exibir relatórios de leitura e nonread gerados pelo repositórios em suas pastas. Armazenando relatórios de leitura e nonread em pastas ocultas permite implementar maior segurança.
  
## <a name="see-also"></a>Confira também



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[Propriedade canônico de PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

