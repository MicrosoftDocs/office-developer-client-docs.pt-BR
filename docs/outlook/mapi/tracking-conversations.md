---
title: Acompanhar conversas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: 'Última modificação: 23 de julho de 2011'
localization_priority: Priority
ms.openlocfilehash: 3a59a7a15b4647832634adc4757544876b8841b1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706216"
---
# <a name="tracking-conversations"></a>Acompanhar conversas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Controle de conversa é coletar respostas a uma mensagem. Clientes devem configurar duas propriedades que auxiliam no controle conversas:
  
- **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))
    
    **PR_CONVERSATION_TOPIC** é o assunto normalizado da mensagem, o assunto sem as cadeias de caracteres de prefixo. Definir esta propriedade para o valor da mensagem **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) propriedade. 
    
- **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))
    
    **PR_CONVERSATION_INDEX** indica a posição de mensagem na conversa específica. É reponsabilidade do cliente configurar **PR_CONVERSATION_INDEX** para cada mensagem de saída seja uma nova mensagem, uma mensagem encaminhada ou uma resposta. Clientes podem defini-la manualmente ou chamar [ScCreateConversationIndex](sccreateconversationindex.md), uma função utilitária fornecida pelo MAPI. 
    
 **ScCreateConversationIndex** gera o valor de um índice da conversa de mensagens de saída. **ScCreateConversationIndex** implementa o índice como um bloqueio de cabeçalho que tem 22 bytes de comprimento, seguido por zero ou mais bloqueio de criança para cada 5 bytes de comprimento. 
  
O bloco de cabeçalho é composto por 22 bytes, divididos em três partes:
  
- Um byte reservado. Esse valor é 1.
    
- Convertidos em cinco bytes para a hora do sistema atual o formato de estrutura [FILETIME](filetime.md). 
    
- Dezesseis bytes segurando um [GUID](guid.md), ou identificador global exclusivo.
    
Cada bloqueio de criança é composto por 5 bytes divididos da seguinte maneira:
  
- Um pouco com um código que representa a diferença entre o horário atual quanto tempo armazenados no bloco de cabeçalho. Este bit será 0 se a diferença é menor do que .02 segundo e maior que dois anos, 1 se a diferença é menor do que um segundo e maior 56 anos.
    
- Trinta e um bits que contém a diferença entre o horário atual e o horário no bloco de cabeçalho expressado nas unidades **FILETIME**. Essa parte do bloco de criança é produzida com uma das duas estratégias, dependendo do valor de bits primeiro. Se esse bits for zero, **ScCreateConversationIndex** descarte os 15 bits mais altos e os 18 bits mais baixos. Se este bit é um, a função descartará bits os 10 bits mais alto e os 23 mais baixos. 
    
- Quatro bits que contém um número aleatório gerado pela função Win32 [ObterContagemMarcaEscala](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx).
    
- Quatro bits com uma contagem de sequência, obtida a partir de um número aleatório.
    
Se você optar por configurar manualmente os índices de conversa de mensagens, considere as seguintes sugestões:
  
1. Manter diferenças em fusos horários dos respondentes transparente; Use UTC vezes em vez de horário local.
    
2. Recue cada grupo de conversa no mesmo valor.
    
3. Classifique respostas na mesma data de mensagem.
    
4. Usar threads separados em momentos diferentes que compartilham o mesmo assunto. 
    
5. Para implementar uma classificação categorizada para que as mensagens sejam agrupadas por tópico, classifique por **PR_CONVERSATION_TOPIC** primeiro e, em seguida, pelo **PR_CONVERSATION_INDEX**. Para apresentar os resultados de classificação, configurar a **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) propriedade 0 por mensagens com um índice da conversa é 22 bytes de comprimento. Em seguida, para cada 5 byte de incremento no tamanho, aumente o valor da propriedade **PR_DEPTH** em um número. 
    
O grupo PR_ORIGINAL das propriedades também pode ser usado para o controle de conversa. Defina essas propriedades para vincular mensagens encaminhadas ou responder a mensagem original. Todas as propriedades PR_ORIGINAL são opcionais. Se você não definir explicitamente, por exemplo, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), o provedor de armazenamento de mensagem pode usar o valor padrão ou o valor da propriedade **PR_ SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)). Da mesma forma, se você não definir **PR_ORIGINAL_AUTHOR_NAME** ou **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), essas propriedades podem ser padrão para os valores a **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) e **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) propriedades, respectivamente. 
  

