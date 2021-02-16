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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415149"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>Propriedade canônica PidTagStoreEntryIdEmsmdbV1

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o estilo antigo (Microsoft Outlook 2002 e versões anteriores) do identificador de entrada de um armazenamento de mensagens do Microsoft Exchange Server 2010 ou do Exchange Server 2013.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Identificador:  <br/> |0x65F60102  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propriedades de ID  <br/> |
   
## <a name="remarks"></a>Comentários

A partir do Microsoft Outlook 2003, os FQDNs do servidor foram integrados às IDs de entrada, evitando RPCs adicionais para indicações. No entanto, isso torna as IDs de entrada mais longas e apresenta mais cenários em que o **método CompareEntryIDs** deve ser usado para determinar se duas IDs de entrada são equivalentes. A PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) acessa o formato mais antigo da ID de entrada do Exchange Server usada pelo Microsoft Outlook 2002 (Microsoft Office XP) e versões anteriores. Isso pode economizar espaço e também reduzir o número de chamadas **CompareEntryIDs** necessárias para determinar quando as IDs de entrada são equivalentes. Observe que usar as IDs de entrada mais antigas para abrir uma caixa de correio pode incorrer em alguns RPCs adicionais se uma referência for necessária. 
  
Para acessar a PR_STORE_ENTRYID_EMSMDB_V1 no modo em cache, você deve ignorar o cache usando o sinalizador MAPI_NO_CACHE com o método [IMAPIProp::GetProps.](imapiprop-getprops.md) Se **PR_STORE_ENTRYID_EMSMDB_V1** não estiver disponível, o código deverá voltar ao PR_STORE_ENTRYID. Somente o Outlook 2003 a Microsoft Outlook 2013 suporta a PR_STORE_ENTRYID_EMSMDB_V1 propriedade. 
  
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

