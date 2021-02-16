---
title: TNEF-Tagged Texto da Mensagem
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
# <a name="tnef-tagged-message-text"></a>TNEF-Tagged Texto da Mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O texto marcado da mensagem é usado pelo TNEF para resolver posições de anexo na mensagem pai. Isso é feito adicionando um espaço reservado no texto da mensagem na posição do anexo. Esse espaço reservado ou marca de anexo descreve o anexo de forma que o TNEF saiba como resolver o anexo e sua posição. As marcas são formatadas da seguinte forma:
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 **\< Título \> do objeto** **\< e nome do \> arquivo** são variáveis que contêm valores que são retirados do anexo em si. Nos casos em que esses valores não estão disponíveis, o título é padrão pelo TNEF com base no tipo de anexo. 
  
A **\< variável KeyNum \>** contém a representação textual da chave de anexo atribuída ao anexo por TNEF. O valor base da chave é passado para a [chamada OpenTnefStreamEx.](opentnefstreamex.md) O valor base não deve ser zero e não deve ser o mesmo para cada chamada para **OpenTnefStreamEx**. Deve ser suficiente usar números pseudo aleatórios com base no tempo do sistema a partir de qualquer gerador de número aleatório que sua biblioteca de tempo de executar fornece, desde que você garanta que eles nunca sejam zero.
  
A **\< \> variável** Transport Name contém o nome do fluxo passado para a chamada [OpenTnefStreamEx](opentnefstreamex.md) ou o valor da propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) .
  
> [!NOTE]
> A **PR_ATTACH_TRANSPORT_NAME** e a variável **\< Transport Name \>** em uma marca de texto de mensagem não têm nada a ver com o nome do provedor de transporte que você está implementando. Esses itens representam o nome de um anexo para o provedor de transporte e o sistema de mensagens. 
  
O texto da mensagem é marcado quando um provedor de transporte solicita um texto de mensagem marcado chamando o método [ITnef::OpenTaggedBody.](itnef-opentaggedbody.md) Ao ler do fluxo de texto marcado, O TNEF substitui o único caractere que estava no texto da mensagem no índice fornecido na propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) pela marca apropriada. Ao escrever no fluxo de texto marcado, o TNEF verifica os dados de entrada em busca de marcas, localiza o anexo associado e substitui a marca por um único caractere de espaço.
  
Observe que, usando o texto marcado da mensagem, um provedor de transporte pode preservar o posicionamento dos anexos, independentemente da maioria das alterações feitas no texto da mensagem pelos sistemas de mensagens.
  

