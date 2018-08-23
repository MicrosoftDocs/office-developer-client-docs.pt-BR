---
title: Texto da mensagem marcado por TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1d514dc8b50183e5d07d71b421a441487e933580
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588857"
---
# <a name="tnef-tagged-message-text"></a>Texto da mensagem marcado por TNEF

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Texto da mensagem marcados é usado pelo TNEF resolver posições de anexo na mensagem pai. Isso é feito com a adição de um espaço reservado no texto da mensagem na posição do anexo. Esse espaço reservado ou marca de anexo, descreve o anexo de tal forma que o TNEF Saiba como resolver o anexo e sua posição. As marcas são formatadas da seguinte maneira:
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 ** \<Título do objeto\> ** e ** \<nome de arquivo\> ** são variáveis que contêm valores que são extraídos do anexo em si. Em casos onde esses valores não estão disponíveis, o título assume o padrão por TNEF com base no tipo de anexo. 
  
O ** \<KeyNum\> ** variável contém a representação textual da chave anexo atribuída ao anexo por TNEF. O valor base da chave é passado na chamada de [OpenTnefStreamEx](opentnefstreamex.md) . O valor de base não deve ser zero e não deve ser o mesmo para cada chamada para **OpenTnefStreamEx**. Ele deve ser suficiente para usar números aleatórios de falsos baseados a hora do sistema de qualquer gerador de números aleatórios fornece em sua biblioteca de tempo de execução, desde que você garante que nunca são zero.
  
O ** \<nome transporte\> ** variável contém o nome de fluxo passado para a chamada de [OpenTnefStreamEx](opentnefstreamex.md) ou o valor da propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
  
> [!NOTE]
> A propriedade **PR_ATTACH_TRANSPORT_NAME** e o ** \<nome transporte\> ** variável em uma marca de texto da mensagem não tem nada a ver com o nome do provedor de transporte que você estiver implementando. Esses itens representam o nome de um anexo para o provedor de transporte e o sistema de mensagens. 
  
O texto da mensagem está marcado quando um provedor de transporte solicita um texto de mensagem marcados chamando o método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) . Ao ler a partir do fluxo de texto marcado, o TNEF substituirá o caractere único que estava no texto da mensagem no índice fornecido na propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) com a marca apropriada. Ao gravar o fluxo de texto marcado, TNEF verifica os dados de entrada de marcas, localiza o anexo associado e substitui a marca com um caractere de espaço simples.
  
Observe que, usando o texto da mensagem marcados, um provedor de transporte pode preservar o posicionamento de anexos independentemente da maioria das alterações feitas para o texto da mensagem por sistemas de mensagens.
  

