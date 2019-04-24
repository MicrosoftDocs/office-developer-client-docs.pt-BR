---
title: Propriedade canônica PidLidToDoOrdinalDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoOrdinalDate
api_type:
- COM
ms.assetid: b6a500fc-07f4-4788-ae46-d179a96a48e2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b0c5e3019efeeb0b9788d81e8730e976bfcc9d75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345273"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a>Propriedade canônica PidLidToDoOrdinalDate

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Determina a ordem de classificação dos objetos em uma lista de tarefas consolidadas.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidToDoOrdinalDate  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085A0  <br/> |
|Tipo de dados:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Tarefa  <br/> |
   
## <a name="remarks"></a>Comentários

Quando um objeto é sinalizado, essa propriedade deve ser definida como a hora atual em tempo universal coordenado (UTC). 
  
Se o cliente permitir que um usuário reordene tarefas dentro da lista de tarefas consolidadas por meio de arrastar ou outros mecanismos, eles poderão usar qualquer algoritmo adequado para determinar o novo valor dessa propriedade para que a tarefa seja exibida no local correto quando essa propriedade for usada como um sor campo de nota.
  
Quando essa propriedade é usada para classificar objetos e a classificação resulta em um objeto tie, a propriedade **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) é usada como um desempate.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica as propriedades e operações relacionadas à sinalização.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

