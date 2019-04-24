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
ms.openlocfilehash: c8bccbfeb7f04745a66831618deff490bc651b02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278768"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>Propriedade canônica PidTagStoreEntryIdEmsmdbV1

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o estilo antigo (Microsoft Outlook 2002 e versões anteriores) do identificador de entrada de um repositório de mensagens do Microsoft Exchange Server 2010 ou Exchange Server 2013.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Identificador:  <br/> |0x65F60102  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propriedades de ID  <br/> |
   
## <a name="remarks"></a>Comentários

A partir do Microsoft Outlook 2003, os FQDNs do servidor foram integrados às IDs de entrada, evitando, assim, RPCss adicionais para indicações. No enTanto, isso torna as IDs de entrada mais longas e introduz mais cenários em que o método **CompareEntryIDs** deve ser usado para determinar se duas identificações de entrada são equivalentes. A propriedade PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) acessa o formato antigo da ID de entrada do servidor Exchange usada pelo Microsoft Outlook 2002 (Microsoft Office XP) e por versões anteriores. Isso pode poupar espaço e também reduzir o número de chamadas **CompareEntryIDs** necessárias para determinar quando as identificações de entrada são equivalentes. Observe que usar as IDs de entrada mais antigas para abrir uma caixa de correio pode gerar RPCs adicionais se for necessária uma referência. 
  
Para acessar a propriedade PR_STORE_ENTRYID_EMSMDB_V1 enquanto estiver no modo cache, você deve ignorar o cache usando o sinalizador MAPI_NO_CACHE com o método [IMAPIProp::](imapiprop-getprops.md) GetProps. Se o **PR_STORE_ENTRYID_EMSMDB_V1** não estiver disponível, o código deverá retornar ao PR_STORE_ENTRYID. Somente o Outlook 2003 por meio do Microsoft Outlook 2013 oferece suporte à propriedade PR_STORE_ENTRYID_EMSMDB_V1. 
  
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

