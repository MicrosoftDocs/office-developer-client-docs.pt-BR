---
title: Propriedade canônica PidLidTaskHistory
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskHistory
api_type:
- COM
ms.assetid: 104ef21c-b607-48b7-9b06-bc53b7d9b68a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 39f2e6aeb4026f0b33be08b3bd8123283e5df3e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303007"
---
# <a name="pidlidtaskhistory-canonical-property"></a>Propriedade canônica PidLidTaskHistory

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica o tipo de alteração que foi feita pela última vez na tarefa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskHistory  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x0000811A  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tarefa  <br/> |
   
## <a name="remarks"></a>Comentários

Quando o valor dessa propriedade é definido, a propriedade **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) também deve ser definida como a hora atual. A tabela a seguir mostra os valores da propriedade **dispidTaskHistory** , listados em ordem de prioridade decrescente. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0x00000004  <br/> |A propriedade **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) foi alterada.  <br/> |
|0x00000003  <br/> |Outra propriedade foi alterada.  <br/> |
|0x00000001  <br/> |O destinatário da tarefa aceitou essa tarefa.  <br/> |
|0x00000002  <br/> |O destinatário da tarefa rejeitou essa tarefa.  <br/> |
|0x00000005  <br/> |A tarefa foi atribuída a um destinatário de tarefa.  <br/> |
|0x00000000  <br/> |Nenhuma alteração foi feita.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

