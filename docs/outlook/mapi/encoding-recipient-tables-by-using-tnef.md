---
title: Codificar tabelas de destinatários usando TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339400"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>Codificar tabelas de destinatários usando TNEF

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A codificação de uma tabela de destinatários para o fluxo de TNEF é raramente necessária, pois a maioria dos sistemas de mensagens dão suporte a listas de destinatários diretamente. Em geral, as propriedades do destinatário são transmitidas no cabeçalho da mensagem. Quando a inclusão da tabela de destinatários é necessária, o TNEF pode codificar a tabela de destinatários como parte de seu processamento normal. Isso é feito durante a fase inicial do processamento TNEF. O provedor de transporte pode incluir a tabela de destinatários da mensagem chamando o método [ITnef::](itnef-addprops.md) addprops com a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) especificada na lista de inclusão. O TNEF Obtém a tabela de destinatários da mensagem, consulta o conjunto de colunas e processa todas as linhas da tabela no fluxo TNEF.
  
Um método alternativo estará disponível se o provedor de transporte precisar modificar a tabela de destinatários antes de ser codificada. O provedor de transporte pode construir a tabela necessária e, em seguida, chamar o método [ITnef:: EncodeRecips](itnef-encoderecips.md) . Se NULL for passado no parâmetro _lpRecipTable_ , a tabela de destinatários será obtida diretamente da mensagem, conforme descrito para **ITnef::** addprops.
  

