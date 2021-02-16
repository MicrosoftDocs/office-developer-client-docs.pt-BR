---
title: Codificando tabelas de destinatários usando o TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417956"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>Codificando tabelas de destinatários usando o TNEF

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A codificação de uma tabela de destinatários no fluxo TNEF raramente é necessária, pois a maioria dos sistemas de mensagens suporta diretamente listas de destinatários. Em geral, as propriedades do destinatário são transmitidas no header da mensagem. Quando a inclusão da tabela de destinatários é necessária, o TNEF pode codificar a tabela de destinatários como parte de seu processamento usual. Isso é feito durante a fase inicial do processamento TNEF. O provedor de transporte pode incluir a tabela de destinatários da mensagem chamando o método [ITnef::AddProps](itnef-addprops.md) com a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) especificada na lista de inclusão. O TNEF obtém a tabela de destinatários da mensagem, consulta o conjunto de colunas e processa todas as linhas da tabela no fluxo TNEF.
  
Um método alternativo estará disponível se o provedor de transporte precisar modificar a tabela de destinatários antes de ser codificada. O provedor de transporte pode construir a tabela necessária e chamar o [método ITnef::EncodeRecips.](itnef-encoderecips.md) Se NULL for passado no parâmetro  _lpRecipTable,_ a tabela de destinatários será retirada diretamente da mensagem, conforme descrito para **ITnef::AddProps**.
  

