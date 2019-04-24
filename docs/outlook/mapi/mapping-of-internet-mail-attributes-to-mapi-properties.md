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
  
Este apêndice descreve como um provedor de transporte MAPI ou um gateway ciente de MAPI que se conecta à Internet deve converter entre propriedades de mensagem MAPI e atributos de mensagem SMTP (Simple Mail Transport Protocol). SMTP é o protocolo de mensagens usado em grande parte da Internet. O SMTP define um conjunto de cabeçalhos de mensagem — o envelope da mensagem — e um formato de conteúdo da mensagem. O SMTP está totalmente documentado em um conjunto de dois documentos, RFC 821 e RFC 822, que podem ser encontrados em vários sites FTP e WWW na Internet.
  
Para obter informações sobre o protocolo SMTP usado para se comunicar com agentes de email baseados em SMTP, consulte RFC 821, "Simple Mail Transfer Protocol [https://www.rfc-editor.org](https://www.rfc-editor.org)", em.
  
Para endereçamento e cabeçalhos de mensagem padrão, consulte RFC 822, "Standard for the formato of ARPA Internet text messages [https://www.rfc-editor.org](https://www.rfc-editor.org)" em.
  
Para MIME, consulte RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: mecanismos para especificar e descrever o formato de corpos de mensagens na Internet," [https://www.rfc-editor.org](https://www.rfc-editor.org)em.
  
O objetivo de mapear atributos de mensagens SMTP para propriedades MAPI (e vice-versa) é garantir que todo o conteúdo de mensagens MAPI, acima e acima, que possa ser codificada usando os atributos de mensagens SMTP nativos, possa ser trocado de forma confiável entre diferentes MAPI componentes que devem se comunicar pela Internet. Este documento baseia-se no trabalho já realizado nesses componentes da Microsoft. 
  
Este documento pressupõe familiaridade com transportes MAPI, TNEF e email SMTP. Ele se esforça para ser conciso, em vez de claro.
  
Como uma convenção, "saída" refere-se a emails de um UA ou MTA compatíveis com MAPI para a Internet, e "entrada" refere-se a emails da Internet para um componente MAPI.
  

