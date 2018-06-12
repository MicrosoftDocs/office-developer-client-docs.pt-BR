---
title: Tabelas de destinatários de codificação usando TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8110eff9b38c76023621f34396d65714a4316d91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766506"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>Tabelas de destinatários de codificação usando TNEF

  
  
**Aplica-se a**: Outlook 
  
A codificação de uma tabela de destinatário no fluxo TNEF raramente é necessária como sistemas de mensagens mais suportam listas destinatários diretamente. Em geral, as propriedades do destinatário são transmitidas no cabeçalho da mensagem. Quando a inclusão da tabela destinatário for necessário, o TNEF pode codificar tabela de destinatário, como parte do seu processamento normal. Isso é feito durante a fase inicial do processamento de TNEF. Provedor de transporte que pode incluir a tabela de destinatário da mensagem chamando o método [ITnef::AddProps](itnef-addprops.md) com a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) especificada na lista de inclusão. TNEF obtém uma tabela de destinatário da mensagem, consulta o conjunto de coluna e processa todas as linhas da tabela no fluxo TNEF.
  
Um método alternativo está disponível se o provedor de transporte precisa modificar a tabela de destinatário antes que ela é codificada. O provedor de transporte pode construir a tabela necessária e então chamar o método [ITnef::EncodeRecips](itnef-encoderecips.md) . Se NULL é passada no parâmetro _lpRecipTable_ , a tabela de destinatários é executada diretamente a partir da mensagem conforme descrito para **ITnef::AddProps**.
  

