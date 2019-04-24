---
title: Propriedade canônica PidLidTaskMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMode
api_type:
- COM
ms.assetid: 185db683-301a-4d91-a583-6959853fa1ad
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d0ae319a6b5fa4c901ec7d318c7ebdd216a2adeb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357936"
---
# <a name="pidlidtaskmode-canonical-property"></a>Propriedade canônica PidLidTaskMode

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica o status da atribuição da tarefa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskMode  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008518  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tarefa  <br/> |
   
## <a name="remarks"></a>Comentários

O valor deve ser um dos seguintes.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0x00000000  <br/> |A tarefa não foi atribuída.  <br/> |
|0x00000001  <br/> |A tarefa é incorporada a uma solicitação de tarefa.  <br/> |
|0x00000002  <br/> |A tarefa foi aceita pelo destinatário da tarefa.  <br/> |
|0x00000003  <br/> |A tarefa foi rejeitada pelo destinatário da tarefa.  <br/> |
|0x00000004  <br/> |A tarefa é incorporada a uma atualização de tarefa.  <br/> |
|0x00000005  <br/> |A tarefa foi atribuída ao destinatário da tarefa.  <br/> |
   
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

