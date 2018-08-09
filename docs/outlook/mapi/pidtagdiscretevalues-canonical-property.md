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
ms.openlocfilehash: 9911d6cee40637a69dfaf432be0e6d42bf38bccd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769200"
---
# <a name="pidtagdiscretevalues-canonical-property"></a>Propriedade canônica PidTagDiscreteValues

  
  
**Aplica-se a**: Outlook 
  
Conterá TRUE se um relatório de não entrega aplica discretos apenas como membros de uma lista de distribuição em vez de toda a lista. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DISCRETE_VALUES  <br/> |
|Identificador:  <br/> |0x0E0E  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |MAPI não transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada dentro de um relatório de não entrega quando a mensagem não pôde ser entregue a um ou mais membros de uma lista de distribuição. Seu objetivo é limitar a retransmissão tenta somente aqueles membros individuais e não a lista de distribuição como um todo. 
  
A tabela de destinatários de um relatório de não entrega contém entradas para todos os destinatários para quem a mensagem não pôde ser entregue e também para as listas de distribuição, se houver, às quais eles pertencem. O provedor de transporte deve definir esta propriedade como TRUE para cada entrada da lista de distribuição, e ele deve copiar o **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e **PR_SEARCH_KEY** ([ PidTagSearchKey](pidtagsearchkey-canonical-property.md)) da lista de distribuição **PR_ORIGINAL_SEARCH_KEY** ([ , **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) e **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)) PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) propriedades para cada membro dessa lista de distribuição. 
  
 **PR_DISCRETE_VALUES** não devem ser definidas para qualquer entrada de destinatários de relatório de não entrega que não seja uma lista de distribuição. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

