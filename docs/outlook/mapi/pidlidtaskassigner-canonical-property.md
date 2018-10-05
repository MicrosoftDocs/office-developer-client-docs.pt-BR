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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400562"
---
# <a name="pidlidtaskassigner-canonical-property"></a>Propriedade canônica PidLidTaskAssigner

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Nomes de usuário que foi a último tarefa atribuída a. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskDelegator  <br/> |
|Propriedade definida:  <br/> |PSETID_Task  <br/> |
|ID de longo (LID):  <br/> |0x00008121  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentários

Se a tarefa não tiver sido atribuída, essa propriedade é da esquerda não definida. Porque o cliente define essa propriedade depois que o destinatário da tarefa recebe uma solicitação de tarefa, a propriedade não será definida na cópia do cedente a tarefa da tarefa. Quando o cliente adiciona ou remove cedente uma tarefa da lista tarefas cedente na propriedade **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)), a propriedade **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) deve ser definido como o adicionado ou cedente de tarefas removidos.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

