---
title: Texto formatado em MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6b82a755cbf2c8bd0f1d3676d4560e131dce3bd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766610"
---
# <a name="formatted-text-in-mapi"></a>Texto formatado em MAPI

  
  
**Aplica-se a**: Outlook 
  
O texto de uma mensagem pode ser armazenado e transmitidas usando texto sem formatação ou texto formatado. Texto formatado aumenta o texto da mensagem, alterar sua aparência com, por exemplo, uma ou mais fontes, tamanhos de fonte ou cores de texto. É recomendável que todos os clientes e sempre que possível, todos os provedores de armazenamento de mensagens, suporte a texto formatado. Com suporte para texto formatado em mensagens agrega valor melhorar a legibilidade de mensagem e fazendo o tratamento de mensagens mais fácil e eficiente.
  
Texto formatado pode ser implementado de diversas maneiras. A maneira mais comum é com o Rich Text Format (RTF). MAPI define três propriedades de transmittable para manter informações de texto da mensagem: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para o texto sem formatação, **PR_HTML** ([Taghtml](pidtaghtml-canonical-property.md)) para HTML e **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) para o texto RTF que tiverem sido compactado. Como a versão formatada de um texto de mensagem pode ser duas vezes tão grande quanto a versão sem a formatação, o texto RTF é compactado antes que sejam transferido com a mensagem e armazenado na propriedade **PR_RTF_COMPRESSED** . Quando é hora de exibir a mensagem na tela, é descompactado usando uma função do utilitário fornecida pelo MAPI. 
  
MAPI define essas duas propriedades de texto de mensagem e mecanismos para conversão entre eles para que os clientes RTF reconhecimento podem interoperar com os clientes e os sistemas de mensagens que não têm suporte para texto formatado.
  
### 

[Sincronizar texto e formatação](synchronizing-text-and-formatting.md)
  
> Descreve como manter o texto da mensagem RTF sincronizado com a formatação.
    
[Suporte a texto formatado em mensagens de saída: responsabilidades do cliente](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> Descreve as responsabilidades do aplicativo cliente para dar suporte a texto formatado em mensagens de saída.
    
[Suporte a texto formatado em mensagens de entrada: responsabilidades do cliente](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> Descreve as responsabilidades do aplicativo cliente para dar suporte a texto formatado em mensagens de entrada.
    
[Suporte a texto formatado: responsabilidades do repositório de mensagens](supporting-formatted-text-message-store-responsibilities.md)
  
> Descreve as responsabilidades do repositório de mensagem para dar suporte a texto formatado.
    
[Suporte a texto formatado: anexos de renderização](supporting-formatted-text-rendering-attachments.md)
  
> Descreve como escolher onde os anexos são processados.
    
[Suporte a texto formatado: responsabilidades do gateway](supporting-formatted-text-gateway-responsibilities.md)
  
> Descreve as responsabilidades do gateway para mensagens de texto formatado de entrada e saída.
    

