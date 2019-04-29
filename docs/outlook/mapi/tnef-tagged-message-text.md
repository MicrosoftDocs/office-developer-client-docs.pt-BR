---
title: Texto da mensagem marcado como TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2b4d4cd790870a024cac6f2ed9952d18a970235a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419916"
---
# <a name="tnef-tagged-message-text"></a>Texto da mensagem marcado como TNEF

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O texto da mensagem marcada é usado pelo TNEF para resolver posições de anexo na mensagem pai. Isso é feito adicionando um espaço reservado no texto da mensagem na posição do anexo. Este espaço reservado, ou marca de anexo, descreve o anexo de tal forma que o TNEF sabe como resolver o anexo e sua posição. As marcas são formatadas da seguinte maneira:
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 O título ** \<\> ** do objeto e o nome do arquivo são variáveis que contêm valores que são obtidos do próprio anexo. ** \<\> ** Nos casos em que esses valores não estão disponíveis, o título é padronizado por TNEF com base no tipo de anexo. 
  
A ** \<variável\> KeyNum** contém a representação textual da chave de anexo atribuída ao anexo por TNEF. O valor base da chave é passado para a chamada [OpenTnefStreamEx](opentnefstreamex.md) . O valor base não deve ser zero e não deve ser o mesmo para todas as chamadas para **OpenTnefStreamEx**. Deve ser suficiente usar números pseudo aleatórios com base no tempo do sistema de qualquer gerador de número aleatório que sua biblioteca de tempo de execução fornece, desde que você garanta que eles nunca sejam zero.
  
A ** \<variável de\> nome de transporte** contém o nome do fluxo passado para a chamada [OpenTnefStreamEx](opentnefstreamex.md) ou o valor da propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
  
> [!NOTE]
> A propriedade **PR_ATTACH_TRANSPORT_NAME** e a ** \<variável de\> nome de transporte** em uma marca de texto de mensagem não têm nada a ver com o nome do provedor de transporte que você está implementando. Estes itens representam o nome de um anexo para o provedor de transporte e o sistema de mensagens. 
  
O texto da mensagem é marcado quando um provedor de transporte solicita um texto da mensagem marcada chamando o método [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) . Ao ler a partir do fluxo de texto marcado, o TNEF substitui o caractere único que estava no texto da mensagem no índice fornecido na propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) com a marca apropriada. Ao gravar no fluxo de texto marcado, o TNEF verifica os dados de entrada para marcas, localiza o anexo associado e substitui a marca por um único caractere de espaço.
  
Observe que, usando o texto da mensagem marcada, um provedor de transporte pode preservar o posicionamento de anexos, independentemente da maioria das alterações feitas no texto da mensagem pelos sistemas de mensagens.
  

