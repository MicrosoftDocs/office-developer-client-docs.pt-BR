---
title: Propriedade canônica PidLidResponseStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0bfa3a01613c49b122e92e4ac281e5b20b5f07ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768631"
---
# <a name="pidlidresponsestatus-canonical-property"></a>Propriedade canônica PidLidResponseStatus

  
  
**Aplica-se a**: Outlook 
  
Especifica o status de resposta de um participante.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidResponseStatus  <br/> |
|Propriedade definida:  <br/> |PSETID_Appointment  <br/> |
|ID de longo (LID):  <br/> |0x00008218  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Reuniões  <br/> |
   
## <a name="remarks"></a>Comentários

O status de resposta deve ser um dos valores na tabela a seguir.
  
|**Status de resposta**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |Nenhuma resposta é necessária para este objeto. Esse é o caso de objetos de compromisso e objetos de resposta de reunião.  <br/> |
|respOrganized  <br/> |0x00000001  <br/> |Esta reunião pertence ao Media Gallery.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Esse valor na reunião do participante indica que o participante aceitou provisoriamente a solicitação de reunião.  <br/> |
|respAccepted  <br/> |0x00000003  <br/> |Esse valor em t de reunião do participante indica que o participante aceitou a solicitação de reunião.  <br/> |
|respDeclined  <br/> |0x00000004  <br/> |Esse valor na reunião do participante indica que o participante recusou a solicitação de reunião.  <br/> |
|respNotResponded  <br/> |0x00000005  <br/> |Esse valor na reunião do participante indica que o nome do participante ainda não tiver respondido. Esse valor é na solicitação de reunião, atualização de reunião e cancelamento de reunião.  <br/> |
   
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

