---
title: Propriedade canônica PidTagOrdinalMost
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOrdinalMost
api_type:
- COM
ms.assetid: c18de08b-8c28-4cdf-bd2e-b9c650cd6da6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 31f39cfbd0e993bfc28003fd64e8af97e7e76818
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329184"
---
# <a name="pidtagordinalmost-canonical-property"></a>Propriedade canônica PidTagOrdinalMost

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um número positivo cujo negativo é menor ou igual ao valor da propriedade **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) de todas as tarefas na pasta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ORDINAL_MOST  <br/> |
|Identificador:  <br/> |0x36E2  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tarefa  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade deve ser atualizada para manter essa condição sempre que a propriedade **dispidTaskOrdinal** de qualquer objeto Task na pasta for alterada de uma forma que viole a condição. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.
  
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

