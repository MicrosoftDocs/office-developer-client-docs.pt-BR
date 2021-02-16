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
ms.openlocfilehash: 3bc475292e47a9ad8dd9565e17640ef95e7b3c76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316678"
---
# <a name="pidlidtaskstartdate-canonical-property"></a>Propriedade canônica PidLidTaskStartDate

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A data em que o usuário espera iniciar a tarefa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskStartDate  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008104  <br/> |
|Tipo de dados:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Tarefas  <br/> |
   
## <a name="remarks"></a>Comentários

Se esse valor de propriedade for deixado desa definida, a tarefa não terá uma data de início. Um valor "0x5AE980E0" (1.525.252.320) também significa que a tarefa não tem uma data de início. Se a tarefa tiver uma data de início, o valor deverá ter um componente de hora da meia-noite, e as propriedades **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) e **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) também deverão ser definidas.
  
Essa propriedade é compartilhada pela Especificação do Protocolo de Sinalização Task-Related Informações e especificação de Protocolo de Objeto Task-Related localizada em [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas em contatos e listas de distribuição pessoais.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedade can�nico de PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)
  
[Propriedade can�nico de PidLidCommonStart](pidlidcommonstart-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

