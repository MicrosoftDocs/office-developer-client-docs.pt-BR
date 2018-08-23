---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6324dcc567aee48f190f8568c6c94b5ee87c731f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584560"
---
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Codifica um modo de exibição da tabela do destinatário da mensagem o fluxo de dados Transport-Neutral Encapsulation Format (TNEF) para a mensagem.
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpRecipientTable_
  
> [in] Um ponteiro para a tabela de destinatários para os quais o modo de exibição é codificado. O parâmetro _lpRecipientTable_ pode ser NULL. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Transporte provedores, provedores de armazenamento de mensagem e o método **ITnef::EncodeRecips** de chamada de gateways para executar a codificação TNEF para um modo de exibição de tabela de destinatário específico. A codificação TNEF é útil, por exemplo, se um provedor ou gateway exige um conjunto específico de colunas, ordem de classificação ou restrição para a tabela de destinatários. 
  
Um provedor ou gateway passa o modo de exibição de tabela a ser codificada no parâmetro _lpRecipientTable_ . A implementação de TNEF codifica a tabela de destinatários com o modo de exibição específico, usando o conjunto específico de colunas, ordem de classificação, restrição e posição. Se um provedor ou gateway transmite NULL no _lpRecipientTable_, TNEF obtém uma tabela de destinatário da mensagem que está sendo codificada usando o método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) , processos e todas as linhas da tabela no fluxo TNEF usando o configurações atuais da tabela. 
  
Assim, chamando **EncodeRecips** com NULL em _lpRecipientTable_ codifica todos os destinatários da mensagem e é equivalente a chamar o método [ITnef::AddProps](itnef-addprops.md) com o sinalizador TNEF_PROP_INCLUDE no seu parâmetro _ulFlags_ e o **PR_ MESSAGE_RECIPIENTS** propriedade ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) no seu parâmetro _lpPropList_ . 
  
Observe que é raramente necessário chamar **EncodeRecips** , a menos que haja um requisito para codificar um modo de exibição de tabela de destinatário específico. Sistemas de mensagens estrangeiro quase sempre têm instalações de manipulação de destinatários listas que são potentes o suficiente para atender às necessidades comuns de codificação de listas de destinatário; Portanto, esses sistemas quase nunca requerem o TNEF para essa finalidade. 
  
## <a name="see-also"></a>Confira também



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[Propriedade canônica PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

