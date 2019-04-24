---
title: Texto formatado em MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7f37d65e4beb328c2c92cf0c2ab28586af6bee45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327465"
---
# <a name="formatted-text-in-mapi"></a>Texto formatado em MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O texto de uma mensagem pode ser armazenado e transmitido usando texto sem formatação ou texto formatado. O texto formatado aprimora o texto da mensagem alterando sua aparência com, por exemplo, uma ou mais fontes, tamanhos de fonte ou cores de texto. É recomendável que todos os clientes e, sempre que possível, todos os provedores de repositórios de mensagens, ofereçam suporte ao texto formatado. O suporte a texto formatado em mensagens agrega valor, melhorando a legibilidade da mensagem e tornando o tratamento de mensagens mais fácil e mais eficiente.
  
O texto formatado pode ser implementado de diversas maneiras. A maneira mais comum é com o formato Rich Text (RTF). MAPI define três propriedades transmittable para armazenar informações de texto da mensagem: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para texto sem formatação, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) para HTML e **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) para texto RTF que tenha sido compactado. Como a versão formatada de um texto de mensagem pode ser duas vezes maior que a versão sem a formatação, o texto RTF é compactado antes de ser transferido com a mensagem e armazenado na propriedade **PR_RTF_COMPRESSED** . Quando é hora de exibir a mensagem na tela, ela é descompactada usando uma função de utilitário fornecida por MAPI. 
  
O MAPI define essas duas propriedades e mecanismos de texto de mensagem para conversão entre eles de forma que os clientes com reconhecimento de RTF possam interoperar com clientes e sistemas de mensagens que não dão suporte a texto formatado.
  
### 

[Sincronização de texto e formatação](synchronizing-text-and-formatting.md)
  
> Descreve como manter o texto da mensagem RTF sincronizado com a formatação.
    
[Suporte a texto formatado em mensagens de saída: responsabilidades do cliente](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> Descreve as responsabilidades do aplicativo cliente para dar suporte ao texto formatado em mensagens de saída.
    
[Suporte a texto formatado em mensagens de entrada: responsabilidades do cliente](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> Descreve as responsabilidades do aplicativo cliente para dar suporte ao texto formatado em mensagens de entrada.
    
[Suporte a texto formatado: responsabilidades do repositório de mensagens](supporting-formatted-text-message-store-responsibilities.md)
  
> Descreve as responsabilidades do repositório de mensagens para dar suporte ao texto formatado.
    
[Suporte a texto formatado: anexos de renderização](supporting-formatted-text-rendering-attachments.md)
  
> Descreve como escolher onde os anexos são renderizados.
    
[Suporte a texto formatado: responsabilidades do gateway](supporting-formatted-text-gateway-responsibilities.md)
  
> Descreve as responsabilidades de gateway para mensagens de texto de saída e de entrada formatadas.
    

