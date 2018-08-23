---
title: Propriedade canônica PidLidTaskStartDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStartDate
api_type:
- COM
ms.assetid: fe87eb3d-21d1-45bb-b848-e141ce1be6a0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b17a5791db4ccb840224785dd71a2ed52143cbaf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565442"
---
# <a name="pidlidtaskstartdate-canonical-property"></a>Propriedade canônica PidLidTaskStartDate

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A data quando o usuário espera para começar a tarefa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskStartDate  <br/> |
|Propriedade definida:  <br/> |PSETID_Task  <br/> |
|ID de longo (LID):  <br/> |0x00008104  <br/> |
|Tipo de dados:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentários

Se o valor dessa propriedade for deixado não definida, a tarefa não tem uma data de início. Um valor igual a "0x5AE980E0" (1,525,252,320) também significa que a tarefa não possui uma data de início. Se a tarefa tiver uma data de início, o valor deve ter um componente de hora de meia-noite e as propriedades de **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) e o **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) também devem ser definidas.
  
Essa propriedade é compartilhada pela especificação do protocolo de sinalização informativos e especificação de protocolo do objeto Task-Related localizados em [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas em contatos e listas de distribuição pessoal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedade can�nico de PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)
  
[Propriedade can�nico de PidLidCommonStart](pidlidcommonstart-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

