---
title: Acompanhar conversas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 58157d597d3bb1042d6bc16ff954495a507c8333
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770621"
---
# <a name="tracking-conversations"></a>Acompanhar conversas

  
  
**Aplica-se a**: Outlook 
  
Acompanhamento de conversa está coletando respostas a uma mensagem. Os clientes devem definir duas propriedades que auxiliam em conversas de acompanhamento:
  
- **PR_CONVERSATION_TOPIC** ([Mapipidtagconversationtopic](pidtagconversationtopic-canonical-property.md))
    
    **PR_CONVERSATION_TOPIC** é normalizado assunto da mensagem, o assunto sem as cadeias de caracteres de prefixo. Defina essa propriedade como o valor da propriedade de **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) da mensagem. 
    
- **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))
    
    **PR_CONVERSATION_INDEX** indica a posição da mensagem em uma conversa em particular. É reponsibility do cliente para definir **PR_CONVERSATION_INDEX** para cada mensagem de saída, seja ela uma nova mensagem, uma mensagem encaminhada ou uma resposta. Os clientes podem definir essa propriedade manualmente ou chamada [ScCreateConversationIndex](sccreateconversationindex.md), a função de um utilitário fornecido pelo MAPI. 
    
 **ScCreateConversationIndex** gera o valor de um índice de conversa de qualquer mensagem de saída. **ScCreateConversationIndex** implementa o índice como um bloco de cabeçalho 22 bytes de comprimento, seguido por zero ou mais filhos bloqueia a cada 5 bytes de comprimento. 
  
O bloco de cabeçalho é composto de 22 bytes, divididos em três partes:
  
- Um byte reservado. Seu valor é 1.
    
- O formato de estrutura [FILETIME](filetime.md) convertidas cinco bytes para a hora atual do sistema. 
    
- Bytes de dezesseis segurando um [GUID](guid.md), ou um identificador globalmente exclusivo.
    
Cada bloco filho é composto de 5 bytes, divididos como segue:
  
- Um bit que contém um código que representa a diferença entre a hora atual e a hora armazenados no bloco de cabeçalho. Esse bit será 0 se a diferença for menor do que:,02 segundo e maior que dois anos e 1 se a diferença for menor do que um segundo e maior 56 anos.
    
- Bits de trinta um contendo a diferença entre a hora atual e a hora no bloco de cabeçalho expressado em unidades de **FILETIME** . Esta parte do bloco filho é produzida usando uma das duas estratégias, dependendo do valor da primeiro estará definido o bit. Se esse bit for zero, **ScCreateConversationIndex** descarta os bits de 15 altos e 18 bits baixos. Se esse bit é aquele, a função descarta os 10 bits altos e os bits de 23 baixos. 
    
- Quatro bits contendo um número aleatório gerado da função Win32 [GetTickCount](http://msdn.microsoft.com/en-us/library/ms724408%28VS.85%29.aspx).
    
- Quatro bits contendo uma contagem de sequência é obtida a parte do número aleatório.
    
Se você optar por definir manualmente os índices de conversa de mensagens, considere as seguintes sugestões:
  
1. Mantenha as diferenças em fusos horários dos entrevistados transparente; Use os tempos de UTC em vez da hora local.
    
2. Recuo de cada grupo de conversação no mesmo valor.
    
3. Respostas de classificação para a mesma data da mensagem.
    
4. Segmentos separados iniciado em momentos diferentes que ocorrem compartilhar o mesmo tópico. 
    
5. Para implementar uma classificação categorizada para que as mensagens são agrupadas por tópico, classificar por **PR_CONVERSATION_TOPIC** primeiro e depois por **PR_CONVERSATION_INDEX**. Para apresentar os resultados da classificação, defina a propriedade **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) como 0 para mensagens com um índice de conversa é 22 bytes de comprimento. Em seguida, para cada incremento de 5 bytes no comprimento, incremente o valor da propriedade **PR_DEPTH** por um. 
    
O grupo PR_ORIGINAL das propriedades também pode ser usado para acompanhamento de conversa. Defina essas propriedades para vincular a responder ou mensagens encaminhadas à mensagem original. Todas as propriedades PR_ORIGINAL são opcionais. Se você não definir explicitamente, por exemplo, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), o provedor de armazenamento de mensagens pode usar o valor padrão, ou o valor de **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) propriedade. Da mesma forma, se você não definir **PR_ORIGINAL_AUTHOR_NAME** ou **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), essas propriedades podem padrão para os valores dos **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) e **PR_ CLIENT_SUBMIT_TIME** propriedades ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)), respectivamente. 
  

