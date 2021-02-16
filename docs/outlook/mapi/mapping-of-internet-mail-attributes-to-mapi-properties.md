---
title: Mapeamento de atributos de email da Internet para propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c0a71cbd3b6cdbef091e75ade5d190369a4626a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355815"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a>Mapeamento de atributos de email da Internet para propriedades MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este apêndice descreve como um provedor de transporte MAPI ou gateway com conhecimento mapi que se conecta à Internet deve ser traduzido entre propriedades de mensagem MAPI e atributos de mensagem SMTP. SMTP é o protocolo de mensagens usado em grande parte da Internet. SMTP define um conjunto de títulos de mensagem — o envelope da mensagem — e um formato de conteúdo de mensagem. O SMTP está totalmente documentado em um conjunto de dois documentos, RFC 821 e RFC 822, que podem ser encontrados em vários sites FTP e WWW na Internet.
  
Para obter informações sobre o protocolo SMTP usado para se comunicar com agentes de email baseados em SMTP, consulte RFC 821, "Simple Mail Transfer Protocol", em [https://www.rfc-editor.org](https://www.rfc-editor.org) .
  
Para endereçamento e os headers de mensagens padrão, consulte RFC 822, "Standard for the Format of ARPA Internet Text Messages", em [https://www.rfc-editor.org](https://www.rfc-editor.org) .
  
Para MIME, consulte RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Parte Um: Mecanismos para especificar e descrever o formato de corpos de mensagens da Internet", em [https://www.rfc-editor.org](https://www.rfc-editor.org) .
  
O objetivo do mapeamento de atributos de mensagem SMTP para propriedades MAPI (e vice-versa) é garantir que todo o conteúdo das mensagens MAPI, acima e acima do que possa ser codificado usando atributos de mensagem SMTP nativos, possa ser trocado de forma confiável entre diferentes componentes MAPI que devem se comunicar pela Internet. Este documento se baseia no trabalho já realizado em tais componentes na Microsoft. 
  
Este documento assume a familiaridade com os emails de transporte MAPI, TNEF e SMTP. Ele se esforça para ser conciso em vez de ser claramente claro.
  
Como convenção, "saída" refere-se a emails que viajam de um UA ou MTA compatível com MAPI para a Internet, e "entrada" refere-se a emails que viajam da Internet para um componente MAPI.
  

