---
title: Propriedade canônica PidLidTaskOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOrdinal
api_type:
- COM
ms.assetid: 1021860e-4c40-4c22-aa68-b568d046aaf7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c3b7c37c800230749f841ba64f4d52cfc9877af0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563650"
---
# <a name="pidlidtaskordinal-canonical-property"></a>Propriedade canônica PidLidTaskOrdinal

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece uma ferramenta para tarefas de classificação personalizadas.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskOrdinal  <br/> |
|Propriedade definida:  <br/> |PSETID_Task  <br/> |
|ID de longo (LID):  <br/> |0x00008123  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ser deixada não definida. Se definido, seu valor deve ser maior que "0x800186A0" (-2,147,383,648) e menor que "0x7FFE7960" (2,147,383,648) e devem ser exclusivos entre tarefas na mesma pasta.
  
Sempre que o cliente define essa propriedade como um número menor do que o negativo do valor da propriedade **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) da pasta atual, o cliente deverá atualizar também **PR_ORDINAL_MOST** na pasta. 
  
A propriedade **PR_ORDINAL_MOST** da pasta proporciona uma maneira eficiente para determinar um valor exclusivo algumas tarefas na mesma pasta. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas. 
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

