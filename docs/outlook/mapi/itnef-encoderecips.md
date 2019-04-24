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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d8caa503e557d35e259db743505d39ea4809dbfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348654"
---
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Codifica um modo de exibição da tabela de destinatários de uma mensagem no fluxo de dados do formato de encapsulamento de transporte neutro (TNEF) para a mensagem.
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Serve deve ser zero.
    
 _lpRecipientTable_
  
> no Um ponteiro para a tabela de destinatários para a qual o modo de exibição é codificado. O parâmetro _lpRecipientTable_ pode ser NULL. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de repositórios de mensagens e gateways chamam o método **ITnef:: EncodeRecips** para executar a codificação TNEF para um determinado modo de exibição de tabela de destinatários. A codificação TNEF é útil, por exemplo, se um provedor ou gateway exigir um determinado conjunto de colunas, ordem de classificação ou restrição para a tabela de destinatários. 
  
Um provedor ou gateway passa o modo de exibição de tabela a ser codificado no parâmetro _lpRecipientTable_ . A implementação do TNEF codifica a tabela de destinatários com o modo de exibição fornecido, usando o conjunto de colunas determinado, a ordem de classificação, a restrição e a posição. Se um provedor ou gateway passar nulos no _lpRecipientTable_, o TNEF Obtém a tabela de destinatários da mensagem que está sendo codificada usando o método [IMessage::](imessage-getrecipienttable.md) GetRecipientTable e processa todas as linhas da tabela para o fluxo TNEF usando o configurações atuais da tabela. 
  
Chamar **EncodeRecips** com nulo no _lpRecipientTable_ , portanto, codifica todos os destinatários da mensagem e é equivalente a chamar o método [ITnef::](itnef-addprops.md) addprops com o sinalizador TNEF_PROP_INCLUDE em seu parâmetro _parâmetroulflags_ e o **PR_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) propriedade em seu parâmetro _lpPropList_ . 
  
Observe que raramente é necessário chamar o **EncodeRecips** , a menos que haja um requisito para codificar um modo de exibição de tabela de destinatário específico. Os sistemas de mensagens estrangeiras quase sempre têm recursos para lidar com listas de destinatários que são poderosas o suficiente para lidar com as necessidades comuns de codificar listas de destinatários; Portanto, esses sistemas quase nunca exigem o TNEF para essa finalidade. 
  
## <a name="see-also"></a>Confira também



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[Propriedade canônica PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

