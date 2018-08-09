---
title: Propriedade canônica PidLidTaskFFixOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFFixOffline
api_type:
- COM
ms.assetid: bbaf7df4-2de0-4da3-9125-eb24dfa94cd8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b8da927fe0080a83748bbb2941979dcb246222fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768708"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a>Propriedade canônica PidLidTaskFFixOffline

  
  
**Aplica-se a**: Outlook 
  
Indica a precisão da propriedade **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskFFixOffline  <br/> |
|Propriedade definida:  <br/> |PSETID_Task  <br/> |
|ID de longo (LID):  <br/> |0x0000812C  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentários

Se a propriedade **dispidTaskFFixOffline** estiver definida como FALSE ou foi removida, o valor da propriedade **dispidTaskOwner** está correto. Se **dispidTaskFFixOffline** for definido como TRUE, o cliente não pode determinar um valor exato para **dispidTaskOwner**. Nesse caso, o cliente pode definir **dispidTaskOwner** para um nome de proprietário genérico, como "Desconhecido". No entanto, se um cliente encontra um valor **dispidTaskFFixOffline** TRUE e pode determinar um nome de proprietário precisas, o cliente deve atualizar **dispidTaskOwner** e defina **dispidTaskFFixOffline** como FALSE. 
  
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

