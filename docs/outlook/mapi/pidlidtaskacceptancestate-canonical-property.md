---
title: Propriedade canônica PidLidTaskAcceptanceState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAcceptanceState
api_type:
- COM
ms.assetid: 7012f524-bc66-48ea-85b5-163e05029d35
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b4124a319f378ff2c60de7a1fddaa549aeb08a05
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583327"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a>Propriedade canônica PidLidTaskAcceptanceState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica o estado de aceitação da tarefa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskDelegValue  <br/> |
|Propriedade definida:  <br/> |PSETID_Task  <br/> |
|ID de longo (LID):  <br/> |0x0000812A  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentários

A tabela a seguir mostra os valores possíveis para essa propriedade.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0x00000000  <br/> |A tarefa não é atribuída.  <br/> |
|0x00000001  <br/> |Status de aceitação da tarefa é desconhecido.  <br/> |
|0x00000002  <br/> |O destinatário da tarefa aceitou a tarefa. Esse valor é definido quando o cliente processa a aceitação de uma tarefa.  <br/> |
|0x00000003  <br/> |O destinatário da tarefa rejeitada a tarefa. Esse valor é definido quando o cliente processa uma rejeição de tarefa.  <br/> |
   
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

