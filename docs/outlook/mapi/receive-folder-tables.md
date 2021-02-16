---
title: Tabelas de Pastas de Recebimento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b291167a0457eaaf4f3bcb48ab36d6c6e6512fcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417347"
---
# <a name="receive-folder-tables"></a>Tabelas de Pastas de Recebimento

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela de pastas de recebimento contém informações para todas as pastas designadas como pastas de recebimento para um armazenamento de mensagens. Uma pasta de recebimento é uma pasta onde as mensagens de entrada de uma classe de mensagem específica são colocadas. Os provedores de repositório de mensagens implementam tabelas de pastas de recebimento e os aplicativos cliente os usam fazendo uma chamada para o método [IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md) 
  
As propriedades a seguir compom o conjunto de colunas necessário nas tabelas da pasta de recebimento:
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

