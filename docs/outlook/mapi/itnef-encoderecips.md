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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437648"
---
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Codifica uma exibição para a tabela de destinatários de uma mensagem no fluxo de dados TNEF (Formato de Encapsulamento Transport-Neutral) da mensagem.
  
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
  
> [in] Um ponteiro para a tabela de destinatários para a qual o exibição é codificado. O  _parâmetro lpRecipientTable_ pode ser NULL. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de armazenamento de mensagens e gateways chamam o método **ITnef::EncodeRecips** para executar a codificação TNEF para um modo de exibição de tabela de destinatário específico. A codificação TNEF é útil, por exemplo, se um provedor ou gateway exigir um determinado conjunto de colunas, ordem de classificação ou restrição para a tabela de destinatários. 
  
Um provedor ou gateway passa o ponto de vista da tabela para ser codificado no parâmetro _lpRecipientTable._ A implementação do TNEF codifica a tabela de destinatários com o modo de exibição determinado, usando o conjunto de colunas determinado, a ordem de classificação, a restrição e a posição. Se um provedor ou gateway passar NULL em  _lpRecipientTable_, TNEF obtém a tabela de destinatário da mensagem que está sendo codificada usando o método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) e processa todas as linhas da tabela para o fluxo TNEF usando as configurações atuais da tabela. 
  
Chamar **EncodeRecips** com NULL em _lpRecipientTable_ codifica todos os destinatários da mensagem e é equivalente a chamar o método [ITnef::AddProps](itnef-addprops.md) com o sinalizador TNEF_PROP_INCLUDE em _seu parâmetro ulFlags_ e a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) em seu parâmetro _lpPropList._ 
  
Observe que raramente é necessário chamar **EncodeRecips,** a menos que haja um requisito para codificar um determinado exibição de tabela de destinatários. Sistemas de mensagens estrangeiros quase sempre têm instalações para lidar com listas de destinatários que são poderosas o suficiente para lidar com as necessidades comuns de codificação de listas de destinatários; portanto, esses sistemas quase nunca exigem TNEF para essa finalidade. 
  
## <a name="see-also"></a>Confira também



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[Propriedade canônica PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

