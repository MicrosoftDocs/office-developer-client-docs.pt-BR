---
title: Suporte a anexos de renderização de texto formatado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68abe85b-5dc0-40d0-8917-30ea002aa816
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5f03530f994fd13e7dc4c7eaa4124900c28e613b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405293"
---
# <a name="supporting-formatted-text-rendering-attachments"></a>Suporte a texto formatado: anexos de renderização

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um aplicativo cliente que se preocupa com o local em que seus anexos são processados define a propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) desses anexos durante a composição da mensagem. Um cliente que não se preocupa com o posicionamento de renderização deixa essa propriedade desdefinida.
  
Quando um cliente abre uma mensagem com anexos, ele tenta recuperar a propriedade **PR_RENDERING_POSITION** de cada anexo para determinar onde no texto da mensagem o anexo deve ser renderizado. Um cliente pode usar um dos seguintes métodos para recuperar o **PR_RENDERING_POSITION**:
  
- [IMAPIProp::](imapiprop-getprops.md) GetProps no anexo aberto para recuperar a propriedade **PR_RENDERING_POSITION** . 
    
- [IMessage::](imessage-getattachmenttable.md) GetAttachmentTable na mensagem aberta para recuperar sua tabela de anexos. **PR_RENDERING_POSITION** é uma coluna obrigatória em todas as tabelas de anexo. Esse é o método preferencial porque resulta em um melhor desempenho. 
    
Os repositórios de mensagens com reconhecimento de RTF podem escolher se desejam retornar um valor exato ou aproximado para **PR_RENDERING_POSITION**. Como os repositórios de mensagens recalculam o valor do **PR_RENDERING_POSITION** de um anexo quando é solicitado pela propriedade **PR_BODY** da mensagem, alguns repositórios de mensagens com reconhecimento de RTF só garantem a precisão das posições de renderização quando um cliente solicita primeiro para **PR_BODY**. Os repositórios de mensagens com reconhecimento de RTF têm permissão para fornecer aos clientes valores de posição de renderização aproximados para melhorar o desempenho. Fornecer uma posição de renderização aproximada e exata poupa tempo e é suficiente para a maioria das situações. 
  
Os repositórios de mensagens com reconhecimento de RTF devem basear sua aproximação no valor especificado pelo cliente responsável pela criação do anexo. Embora todos os clientes devam definir o **PR_RENDERING_POSITION**, os provedores de repositórios de mensagens devem estar preparados para lidar com a possibilidade de sua ausência. Quando o cliente não define **PR_RENDERING_POSITION**, um repositório de mensagens pode defini-lo como-1 para indicar que a posição de renderização não está dentro do texto da mensagem. Anexos com uma posição de renderização de-1 podem ser exibidos em qualquer lugar dentro da mensagem, dependendo do cliente. Muitos clientes posicionam esses tipos de anexos na parte superior da mensagem.
  
O grau de precisão para uma propriedade **PR_RENDERING_POSITION** depende se um repositório de mensagens salvará ou não as propriedades de uma mensagem de **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) e **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou somente **PR_RTF_COMPRESSED**. Se o cliente gerar **PR_BODY** e o repositório de mensagens salvá-lo junto com o texto formatado, as posições de renderização serão precisas. No enTanto, se o repositório de mensagens deve gerar sua própria versão do **PR_BODY** porque ele só salva **PR_RTF_COMPRESSED**, é provável que as posições de renderização sejam um pouco imprecisas. Isso ocorre devido às diferenças no modo como os clientes e os provedores de repositórios de mensagens geram a propriedade **PR_BODY** . 
  
Para calcular um valor **PR_RENDERING_POSITION** preciso, um repositório com reconhecimento de RTF usa uma marca incorporada no texto formatado. A função de utilitário **RTFSync** pode ser chamada para executar esse cálculo e atualizar a posição de renderização de um anexo. Dependendo da quantidade de informações de estado disponíveis, o repositório de mensagens pode passar RTF_SYNC_BODY_CHANGED, RTF_SYNC_RTF_CHANGED ou ambos os valores para [RTFSync](rtfsync.md).
  

