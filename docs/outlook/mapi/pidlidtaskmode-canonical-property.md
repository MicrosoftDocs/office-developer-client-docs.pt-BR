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
ms.openlocfilehash: bc8e4dfe934d516c07d5532ba6a95e51a3cbf962
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578077"
---
# <a name="pidlidtaskmode-canonical-property"></a>Propriedade canônica PidLidTaskMode

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica o status de atribuição da tarefa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskMode  <br/> |
|Propriedade definida:  <br/> |PSETID_Common  <br/> |
|ID de longo (LID):  <br/> |0x00008518  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentários

O valor deve ser um destes procedimentos.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0x00000000  <br/> |A tarefa não é atribuída.  <br/> |
|0x00000001  <br/> |A tarefa está incorporada em uma solicitação de tarefa.  <br/> |
|0x00000002  <br/> |A tarefa foi aceita pelo destinatário da tarefa.  <br/> |
|0x00000003  <br/> |A tarefa foi rejeitada pelo destinatário da tarefa.  <br/> |
|0x00000004  <br/> |A tarefa está incorporada em uma atualização de tarefa.  <br/> |
|0x00000005  <br/> |A tarefa foi atribuída ao cedente a tarefa.  <br/> |
   
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

