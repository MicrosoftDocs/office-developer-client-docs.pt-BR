---
title: Mapeamento dos atributos de email da Internet para propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c0a71cbd3b6cdbef091e75ade5d190369a4626a4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400364"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a>Mapeamento dos atributos de email da Internet para propriedades MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este apêndice descreve como um provedor de transporte MAPI ou gateway reconhecimento de MAPI que se conecta à Internet deve traduzir entre os atributos de mensagem do protocolo de transporte de email simples (SMTP) e propriedades de mensagem MAPI. SMTP é o protocolo de mensagens usado em grande parte da Internet. SMTP define um conjunto de cabeçalhos de mensagem — o envelope da mensagem — e um formato de conteúdo da mensagem. SMTP está documentada em um conjunto de dois documentos, RFC 821 e RFC 822, que pode ser encontrado em um número de sites FTP e WWW na Internet.
  
Para obter informações sobre o protocolo SMTP usado para se comunicar com os agentes de email baseados em SMTP, consulte RFC 821, "Simple Mail Transfer Protocol," em [https://www.rfc-editor.org](https://www.rfc-editor.org).
  
Para cabeçalhos de mensagem padrão e endereçamento, consulte RFC 822, "Padrão para o formato de ARPA Internet Text Messages," em [https://www.rfc-editor.org](https://www.rfc-editor.org).
  
Para MIME, consulte RFC 1521, "parte MIME (Multipurpose Internet Mail Extensions) um: mecanismos para especificando e descrevendo o formato dos corpos de mensagens da Internet," em [https://www.rfc-editor.org](https://www.rfc-editor.org).
  
O objetivo do mapeamento de atributos de mensagem SMTP para propriedades MAPI (e vice-versa) é garantir que todo o conteúdo das mensagens MAPI, além do que o que pode ser codificada atributos de mensagem SMTP nativos, pode ser trocado confiável entre diferente MAPI componentes que devem se comunicar pela Internet. Este documento baseia-se no trabalho já realizado em tais componentes na Microsoft. 
  
Este documento pressupõe familiaridade com transportes MAPI, TNEF e SMTP mail. Ela se esforça para ser conciso em vez de muito claro.
  
Como uma convenção, "saída" refere-se para viagem de um UA compatível com MAPI ou MTA à Internet de email e "entrada" refere-se ao correio viajar da Internet para um componente MAPI.
  

