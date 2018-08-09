---
title: Propriedade canônica PidTagStoreEntryIdEmsmdbV1
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 74626b735599a5f1485b26fcb65d907b552b3089
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770083"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>Propriedade canônica PidTagStoreEntryIdEmsmdbV1

  
  
**Aplica-se a**: Outlook 
  
Contém o estilo antigo (Microsoft Outlook 2002 e versões anteriores) do identificador de entrada de um armazenamento de mensagens do Microsoft Exchange Server 2010 ou Exchange Server 2013.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Identificador:  <br/> |0x65F60102  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propriedades de identificação  <br/> |
   
## <a name="remarks"></a>Comentários

Começando com o Microsoft Outlook 2003, os FQDNs de servidor foram integrados nas identificações de entrada, evitando RPCs adicionais para referências. No entanto, isso torna mais de identificações de entrada e introduz mais cenários em que o método **CompareEntryIDs** deve ser usado para determinar se dois entrada IDs são equivalentes. O PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) propriedade acessa o formato mais antigo da identificação de entrada do Exchange Server usada pelo Microsoft Outlook 2002 (Microsoft Office XP) e versões anteriores. Isso pode economizar espaço e também reduzir o número de chamadas **CompareEntryIDs** necessários para determinar quando a entrada IDs são equivalentes. Observe que usando a entrada mais antiga IDs para abrir uma caixa de correio pode incorrer em alguns RPCs adicionais se uma referência é necessária. 
  
Para acessar a propriedade PR_STORE_ENTRYID_EMSMDB_V1 enquanto estiver no modo de cache, você deve ignorar o cache usando o sinalizador MAPI_NO_CACHE com o método [IMAPIProp::GetProps](imapiprop-getprops.md) . Se **PR_STORE_ENTRYID_EMSMDB_V1** não estiver disponível, o código deve descriptografado PR_STORE_ENTRYID. Somente o Outlook 2003 por meio do Microsoft Outlook 2013 suporta a propriedade PR_STORE_ENTRYID_EMSMDB_V1. 
  
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

