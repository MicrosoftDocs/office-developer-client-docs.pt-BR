---
title: Propriedade canônica PidLidToAttendeesString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToAttendeesString
api_type:
- COM
ms.assetid: ca1eedba-c617-4403-8490-315ab75f2edb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 75439fccaf13665c68321cac5d39d0373ca923e1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571091"
---
# <a name="pidlidtoattendeesstring-canonical-property"></a>Propriedade canônica PidLidToAttendeesString

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma lista de todos os participantes sendable que também são participantes necessários.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidToAttendeesString  <br/> |
|Propriedade definida:  <br/> |PSETID_Appointment  <br/> |
|ID de longo (LID):  <br/> |0x0000823B  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Reuniões  <br/> |
   
## <a name="remarks"></a>Comentários

O valor para cada participante é a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do participante catálogo de endereços. Entradas separadas devem ser delimitadas por ponto e vírgula seguido por um espaço. Essa propriedade não é necessária.
  
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

