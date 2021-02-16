---
title: Propriedade canônica PidLidAutoFillLocation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAutoFillLocation
api_type:
- COM
ms.assetid: e4db6cae-4730-45d0-8b8a-9bd484c8bd3f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2d1edf371486c5db0aa8b869726c8a9a7b62ab06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344993"
---
# <a name="pidlidautofilllocation-canonical-property"></a>Propriedade canônica PidLidAutoFillLocation

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica que o valor da propriedade **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) é definido como a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do RecipientRow que representa um recurso.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidAutoFillLocation  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x0000823A  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Reuniões  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter mais detalhes sobre RecipientRow, consulte o protocolo de Objeto de Mensagem e Anexo conforme especificado em [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

