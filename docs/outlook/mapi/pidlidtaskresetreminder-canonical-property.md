---
title: Propriedade canônica PidLidTaskResetReminder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskResetReminder
api_type:
- COM
ms.assetid: f6da69ff-a913-4a65-bb07-8ad3c5685e5e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9a438fb2b1862d44905a63fda3e5f68b7878cd99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316615"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a>Propriedade canônica PidLidTaskResetReminder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica se futuras instâncias de tarefas recorrentes precisam de lembretes, mesmo que **dispidReminderSet** ([PIDLIDREMINDERSET](pidlidreminderset-canonical-property.md)) seja falso.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskResetReminder  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008107  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Tarefa  <br/> |
   
## <a name="remarks"></a>Comentários

Esse valor é definido como TRUE quando o lembrete da tarefa é ignorado e, caso contrário, é definido como FALSE. Se a redefinição à esquerda, um padrão FALSE será adotado.
  
Conforme especificado em [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), a propriedade **dispidReminderSet** indica se um lembrete está definido na tarefa. No enTanto, essa propriedade indica apenas a presença de um lembrete em uma única tarefa. Ele não pode ser usado sozinho para determinar se uma instância futura de uma tarefa recorrente precisa de um lembrete. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Especifica as propriedades e o modelo de interação para email e outros lembretes de objeto.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedade can�nico de PidLidReminderSet](pidlidreminderset-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

