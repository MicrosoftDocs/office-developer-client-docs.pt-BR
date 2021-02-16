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
ms.openlocfilehash: a64008da93584529916a9303176bba0aa08d3fac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357957"
---
# <a name="pidlidtaskordinal-canonical-property"></a>Propriedade canônica PidLidTaskOrdinal

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece um auxílio para tarefas de classificação personalizadas.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskOrdinal  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008123  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tarefas  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ser deixada desalinhada. Se definido, seu valor deve ser maior que "0x800186A0" (-2.147.383.648) e menor que "0x7FFE7960" (2.147.383.648) e deve ser exclusivo entre tarefas na mesma pasta.
  
Sempre que o cliente define essa propriedade como um número menor que o negativo do valor atual da propriedade **PR_ORDINAL_MOST** (  [PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) da pasta, o cliente também deve atualizar PR_ORDINAL_MOST na pasta. 
  
A **PR_ORDINAL_MOST** propriedade da pasta fornece uma maneira eficiente de determinar um valor exclusivo entre tarefas na mesma pasta. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas. 
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

