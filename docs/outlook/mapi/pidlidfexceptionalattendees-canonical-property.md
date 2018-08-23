---
title: Propriedade canônica PidLidFExceptionalAttendees
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalAttendees
api_type:
- COM
ms.assetid: f1f489a3-e83a-4e96-bf9a-d98bc17d29f5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 68ad6bd888594d09ab8e1dac050f8181341f7ee4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570776"
---
# <a name="pidlidfexceptionalattendees-canonical-property"></a>Propriedade canônica PidLidFExceptionalAttendees

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica se esta propriedade é um objeto calendar recorrente com um ou mais exceções e pelo menos uma das mensagens de exceção incorporada tem pelo menos um RecipientRow.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidFExceptionalAttendees  <br/> |
|Propriedade definida:  <br/> |PSETID_Appointment  <br/> |
|ID de longo (LID):  <br/> |0x0000822B  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Reuniões  <br/> |
   
## <a name="remarks"></a>Comentários

A ausência dessa propriedade, ou um valor FALSE indica que o objeto calendar tem sem exceções, ou nenhuma das mensagens de exceção incorporada tem RecipientRows.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

