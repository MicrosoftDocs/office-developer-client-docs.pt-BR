---
title: Propriedade canônica PidLidAppointmentColor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentColor
api_type:
- COM
ms.assetid: 91147e85-f440-4463-850b-efc9bdbd36d1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 251377a7b9118437aff3fbb6b2b9376cbf70375c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768209"
---
# <a name="pidlidappointmentcolor-canonical-property"></a>Propriedade canônica PidLidAppointmentColor

  
  
**Aplica-se a**: Outlook 
  
Especifica a cor a ser usada ao exibir o calendário.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidApptColor  <br/> |
|Propriedade definida:  <br/> |PSETID_Appointment  <br/> |
|ID de longo (LID):  <br/> |0x00008214  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade especifica a cor a ser usada ao exibir o calendário. Um cliente ou servidor deve definir esse valor para manter a compatibilidade com clientes mais antigos. Em vez disso, ele pode exibir o calendário baseado no valor da propriedade de **palavras-chave** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) como especificado em [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx). Quando definido, o valor deve ser um destes procedimentos.
  
|**Valor**|**Color**|
|:-----|:-----|
|0x00000000  <br/> |Nenhum  <br/> |
|0x00000001  <br/> |Vermelho  <br/> |
|0x00000002  <br/> |Azul  <br/> |
|0x00000003  <br/> |Verde  <br/> |
|0x00000004  <br/> |Cinza  <br/> |
|0x00000005  <br/> |Laranja  <br/> |
|0x00000006  <br/> |Ciano  <br/> |
|0x00000007  <br/> |Verde-oliva  <br/> |
|0x00000008  <br/> |Roxo  <br/> |
|0x00000009  <br/> |Azul-petróleo  <br/> |
|0x0000000A  <br/> |Amarelo  <br/> |
   
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

