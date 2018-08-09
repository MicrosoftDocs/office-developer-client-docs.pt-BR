---
title: Receber tabelas de pastas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5f3bcda3beb29fa91629ea1639522ef24dc6eb32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770216"
---
# <a name="receive-folder-tables"></a>Receber tabelas de pastas

  
  
**Aplica-se a**: Outlook 
  
Uma tabela de pasta de recebimento contém informações para todas as pastas designadas como pastas de recebimento para um armazenamento de mensagens. Uma pasta de recebimento é uma pasta em que as mensagens recebidas de uma classe de mensagem específica são colocadas. Tabelas de pasta de recebimento de implementar de provedores de repositório de mensagem e aplicativos cliente usá-las fazendo uma chamada ao método [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
A seguintes propriedades formam a coluna necessária definir em receber tabelas de pasta:
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

