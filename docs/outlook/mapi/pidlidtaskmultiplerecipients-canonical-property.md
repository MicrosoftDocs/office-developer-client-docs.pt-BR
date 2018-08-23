---
title: Propriedade canônica PidLidTaskMultipleRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMultipleRecipients
api_type:
- COM
ms.assetid: 28ba9997-72dd-465f-94a7-35a317a361ef
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f20c3e988c0a0461a966a109a8d345c22e1fccee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585735"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a>Propriedade canônica PidLidTaskMultipleRecipients

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece dicas de otimização sobre os destinatários de uma tarefa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskMultRecips  <br/> |
|Propriedade definida:  <br/> |PSETID_Task  <br/> |
|ID de longo (LID):  <br/> |0x00008120  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentários

Se definido, essa propriedade deverá ser definida como uma operação **OR** bit a bit de zero ou mais dos seguintes valores. 
  
|**Name**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|Enviado  <br/> |0x00000001  <br/> |A tarefa possui vários destinatários principais.  <br/> |
|Received  <br/> |0x00000002  <br/> |Embora a dica Sent não estava presente, o cliente detectou que a tarefa tem vários destinatários principais.  <br/> |
|Reservado  <br/> |0x00000004  <br/> |Esse valor é reservado.  <br/> |
   
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

