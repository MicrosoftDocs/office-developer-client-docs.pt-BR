---
title: Propriedade canônica PidTagDiscreteValues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscreteValues
api_type:
- HeaderDef
ms.assetid: 958f3cf7-953a-43f4-9102-ad35edf5e813
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6d6974302e3413db3590abbbd3e6567976c6ac72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360820"
---
# <a name="pidtagdiscretevalues-canonical-property"></a>Propriedade canônica PidTagDiscreteValues

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém TRUE se um relatório de não entrega só se aplica a membros discretos de uma lista de distribuição, e não à lista inteira. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DISCRETE_VALUES  <br/> |
|Identificador:  <br/> |0x0E0E  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |MAPI não-transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada em um relatório de não entrega quando a mensagem não pôde ser entregue a um ou mais membros de uma lista de distribuição. Sua finalidade é limitar as tentativas de retransmissão a apenas os membros individuais e não à lista de distribuição como um todo. 
  
A tabela de destinatários de um relatório de não entrega contém entradas para todos os destinatários aos quais a mensagem não pôde ser entregue e também para as listas de distribuição, se houver, às quais pertencem. O provedor de transporte deve definir essa propriedade como TRUE para cada entrada de lista de distribuição e deve copiar o **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e **PR_SEARCH_KEY** ([ PidTagSearchKey](pidtagsearchkey-canonical-property.md)) da lista de distribuição para o **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) e **PR_ORIGINAL_SEARCH_KEY** ([ PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) para cada membro dessa lista de distribuição. 
  
 **PR_DISCRETE_VALUES** não deve ser definido para qualquer entrada de destinatário de relatório de não entrega que não seja uma lista de distribuição. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

