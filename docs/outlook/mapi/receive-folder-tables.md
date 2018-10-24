---
title: Receber tabelas de pastas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b88545ede6275bd834fad5869d972e2860a6c77e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573177"
---
# <a name="receive-folder-tables"></a>Receber tabelas de pastas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela de pasta de recebimento contém informações para todas as pastas designadas como pastas de recebimento para um armazenamento de mensagens. Uma pasta de recebimento é uma pasta em que as mensagens recebidas de uma classe de mensagem específica são colocadas. Tabelas de pasta de recebimento de implementar de provedores de repositório de mensagem e aplicativos cliente usá-las fazendo uma chamada ao método [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
A seguintes propriedades formam a coluna necessária definir em receber tabelas de pasta:
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

