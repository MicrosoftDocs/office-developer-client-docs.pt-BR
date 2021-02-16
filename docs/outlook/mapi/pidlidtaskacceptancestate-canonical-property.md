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
ms.openlocfilehash: b42be4b42d085aba8999a8c3f1a780ed972fa136
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331287"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a>Propriedade canônica PidLidTaskAcceptanceState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica o estado de aceitação da tarefa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskDelegValue  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x0000812A  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tarefas  <br/> |
   
## <a name="remarks"></a>Comentários

A tabela a seguir mostra os valores possíveis para essa propriedade.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0x00000000  <br/> |A tarefa não é atribuída.  <br/> |
|0x00000001  <br/> |O status de aceitação da tarefa é desconhecido.  <br/> |
|0x00000002  <br/> |O destinatário da tarefa aceitou a tarefa. Esse valor é definido quando o cliente processa uma aceitação da tarefa.  <br/> |
|0x00000003  <br/> |O destinatário da tarefa rejeitou a tarefa. Esse valor é definido quando o cliente processa uma rejeição de tarefa.  <br/> |
   
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

