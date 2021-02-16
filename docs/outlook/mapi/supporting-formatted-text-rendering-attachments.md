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
# <a name="supporting-formatted-text-rendering-attachments"></a>Suporte a texto formatado: renderização de anexos

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um aplicativo cliente que sabe onde em uma mensagem seus anexos são renderizados define a propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) para esses anexos durante a composição da mensagem. Um cliente que não se importa com o posicionamento da renderização deixa essa propriedade sem colocação.
  
Quando um cliente abre uma mensagem com anexos,  ele tenta recuperar a propriedade PR_RENDERING_POSITION de cada anexo para determinar onde, no texto da mensagem, o anexo deve ser renderizado. Um cliente pode usar um dos seguintes métodos para **recuperar** PR_RENDERING_POSITION:
  
- [IMAPIProp::GetProps](imapiprop-getprops.md) no anexo aberto para recuperar a **PR_RENDERING_POSITION** propriedade. 
    
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) na mensagem aberta para recuperar sua tabela de anexos. **PR_RENDERING_POSITION** é uma coluna necessária em todas as tabelas de anexos. Esse é o método preferencial porque resulta em um melhor desempenho. 
    
Os armazenamentos de mensagens com conhecimento RTF podem optar por retornar um valor preciso ou aproximado **para PR_RENDERING_POSITION**. Como os armazenamentos de mensagens recalculam o valor de PR_RENDERING_POSITION de um anexo quando solicitado a propriedade **PR_BODY da** mensagem, alguns armazenamentos de mensagens com conhecimento RTF garantem apenas **a** precisão das posições de renderização quando um cliente solicita primeiro PR_BODY **.** Os armazenamentos de mensagens com suporte a RTF têm permissão para fornecer aos clientes valores aproximados de posição de renderização para melhorar o desempenho. Fornecer uma posição aproximada em vez de uma posição de renderização precisa economiza tempo e é suficiente para a maioria das situações. 
  
Os armazenamentos de mensagens com conhecimento RTF devem basear sua aproximação no valor especificado pelo cliente responsável pela criação do anexo. Embora todos os clientes devam **PR_RENDERING_POSITION**, os provedores do armazenamento de mensagens devem estar preparados para lidar com a possibilidade de sua ausência. Quando o cliente não PR_RENDERING_POSITION **,** um armazenamento de mensagens pode defini-lo como -1 para indicar que a posição de renderização não está dentro do texto da mensagem. Anexos com uma posição de renderização de -1 podem ser exibidos em qualquer lugar dentro da mensagem, dependendo do cliente. Muitos clientes posicionam esses tipos de anexos na parte superior da mensagem.
  
O grau de precisão de uma propriedade **PR_RENDERING_POSITION** depende de um armazenamento de mensagens salvar ou não as propriedades **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) e **PR_RTF_COMPRESSED** ([PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)de uma mensagem ou apenas **PR_RTF_COMPRESSED**. Se o cliente gerar **PR_BODY** e o armazenamento de mensagens salvá-lo junto com o texto formatado, as posições de renderização serão precisas. No entanto, se o armazenamento de mensagens deve gerar sua própria versão do **PR_BODY** porque ele só salva **PR_RTF_COMPRESSED**, é provável que as posições de renderização sejam um pouco imprecisas. Isso se deve às diferenças na maneira como os clientes e provedores de armazenamento de mensagens geram a **PR_BODY** propriedade. 
  
Para calcular um valor **PR_RENDERING_POSITION,** um armazenamento com conhecimento RTF usa uma marca inserida no texto formatado. A função utilitário **RTFSync** pode ser chamada para executar esse cálculo e atualizar a posição de renderização de um anexo. Dependendo da quantidade de informações de estado disponíveis, o armazenamento de mensagens pode passar RTF_SYNC_BODY_CHANGED, RTF_SYNC_RTF_CHANGED ou ambos os valores para [RTFSync](rtfsync.md).
  

