---
title: Texto formatado anexos de renderização de suporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68abe85b-5dc0-40d0-8917-30ea002aa816
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1b6339d768ac476c24ce988ba761270a50d47464
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580310"
---
# <a name="supporting-formatted-text-rendering-attachments"></a>Suporte a texto formatado: anexos de renderização

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um aplicativo cliente que se importa onde em uma mensagem em seus respectivos anexos são renderizados define a propriedade de **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) para esses anexos durante composição de mensagem. Um cliente que não está preocupado posicionamento de renderização deixa essa propriedade não definidas.
  
Quando um cliente abre uma mensagem com anexos, ele tenta recuperar a propriedade **PR_RENDERING_POSITION** de cada anexo para determinar onde no texto da mensagem o anexo deve ser renderizado. Um cliente pode usar um dos métodos a seguir para recuperar **PR_RENDERING_POSITION**:
  
- [IMAPIProp::GetProps](imapiprop-getprops.md) no anexo abrir para recuperar a propriedade **PR_RENDERING_POSITION** . 
    
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) na mensagem de abrir para recuperar sua tabela de anexo. **PR_RENDERING_POSITION** é uma coluna necessária em todas as tabelas de anexo. Este é o método preferencial porque ele implica em um melhor desempenho. 
    
Repositórios de mensagem RTF reconhecimento podem escolher se deve retornar um valor preciso ou aproximado para **PR_RENDERING_POSITION**. Porque a mensagem repositórios recalcular o valor de **PR_RENDERING_POSITION** um anexo quando for solicitado para a propriedade **PR_BODY** da mensagem, alguns mensagem RTF reconhecimento armazena garantia apenas a precisão dos posições de renderização quando um cliente solicita primeiro **PR_BODY**. Repositórios de mensagem RTF reconhecimento têm permissão para fornecer a clientes com valores de posição de renderização aproximado para aprimorar o desempenho. Fornecer uma aproximado em vez de uma posição de renderização precisas economiza tempo e é suficiente para a maioria das situações. 
  
Repositórios de mensagem RTF reconhecimento devem basear seu aproximação no valor especificado pelo cliente responsável por criar o anexo. Embora todos os clientes devem definir **PR_RENDERING_POSITION**, provedores de armazenamento de mensagem devem estar preparados para lidar com a possibilidade de sua ausência. Quando o cliente não definida **PR_RENDERING_POSITION**, um armazenamento de mensagens poderá defini-la como -1 para indicar que a posição de renderização não está dentro do texto da mensagem. Anexos com uma posição de renderização de -1 podem ser exibidos em qualquer lugar dentro da mensagem, dependendo do cliente. Muitos clientes posicionar esses tipos de anexos na parte superior da mensagem.
  
O grau de precisão para uma propriedade **PR_RENDERING_POSITION** depende se ou não um armazenamento de mensagens salva **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) uma mensagem e as propriedades de **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou somente **PR_RTF_COMPRESSED**. Se o cliente gera **PR_BODY** e o armazenamento de mensagens salva juntamente com o texto formatado, as posições de renderização será precisas. No entanto, se o armazenamento de mensagens deve gerar sua própria versão do **PR_BODY** porque ele salva somente **PR_RTF_COMPRESSED**, é provável que seja relativamente imprecisas as posições de renderização. Isso é devido às diferenças da maneira que os clientes e os provedores de armazenamento de mensagem geram a propriedade **PR_BODY** . 
  
Para calcular um valor exato da **PR_RENDERING_POSITION** , um armazenamento de reconhecimento de RTF usa uma marca incorporada o texto formatado. A função do utilitário **RTFSync** pode ser chamada para realizar esse cálculo e atualizar posição de renderização de um anexo. Dependendo da quantidade de informações de estado disponíveis, o armazenamento de mensagens pode passar RTF_SYNC_BODY_CHANGED, RTF_SYNC_RTF_CHANGED ou ambos os valores para [RTFSync](rtfsync.md).
  

