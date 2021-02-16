---
title: Propriedade canônica PidLidTaskAssigner
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigner
api_type:
- COM
ms.assetid: f7047e4e-0fb3-476b-9568-8f1135e6d970
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ef5f78fa36632227311d037ee61085c677920fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340086"
---
# <a name="pidlidtaskassigner-canonical-property"></a>Propriedade canônica PidLidTaskAssigner

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Nomeia o usuário que foi atribuído pela última vez à tarefa. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskDelegator  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008121  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Tarefas  <br/> |
   
## <a name="remarks"></a>Comentários

Se a tarefa não tiver sido atribuída, essa propriedade será deixada desanhada. Como o cliente define essa propriedade depois que o destinatário da tarefa recebe uma solicitação de tarefa, a propriedade não será definida na cópia da tarefa do destinatário da tarefa. Quando o cliente adiciona ou remove um atribuídor de tarefa da lista de atribuição de tarefas na propriedade **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)), a **propriedade dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) deve ser definida para o atribuídor de tarefa adicionado ou removido.
  
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

