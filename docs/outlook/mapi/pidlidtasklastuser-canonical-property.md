---
title: Propriedade canônica PidLidTaskLastUser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastUser
api_type:
- COM
ms.assetid: 914c55e9-cb36-46a4-b5ee-382413fa25f9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 76311a76001b122bdfd984b9dedc37c2ff878fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360442"
---
# <a name="pidlidtasklastuser-canonical-property"></a>Propriedade canônica PidLidTaskLastUser

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Nomeia o usuário mais recente que era o proprietário da tarefa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskLastUser  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008122  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Tarefas  <br/> |
   
## <a name="remarks"></a>Comentários

Antes de um cliente enviar uma solicitação de tarefa, ele define essa propriedade com o nome do atribuídor de tarefa. Antes de um cliente enviar uma aceitação da tarefa, ele define essa propriedade como o nome do destinatário da tarefa. Antes de um cliente enviar uma rejeição de tarefa, ele define essa propriedade com o nome do atribuídor de tarefa.
  
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

