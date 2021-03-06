---
title: Propriedade canônica PidLidCleanGlobalObjectId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c48fa333d407492b69da5287fa75c565bfd10e11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349214"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a>Propriedade canônica PidLidCleanGlobalObjectId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica o ObjectID global **limpo.**
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidCleanGlobalObjId  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Meeting  <br/> |
|Long ID (LID):  <br/> |0x00000023  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Reuniões  <br/> |
   
## <a name="remarks"></a>Comentários

O formato dessa propriedade é o mesmo de **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)). O valor dessa propriedade deve ser igual ao valor de **LID_GLOBAL_OBJID**, exceto os campos YH, YL, M e D devem ser zero. Todos os objetos que se referem a uma Instância de uma série recorrente (incluindo uma instância órfã), bem como a própria série recorrente, terão o mesmo valor para essa propriedade.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

