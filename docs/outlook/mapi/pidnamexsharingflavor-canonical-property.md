---
title: Propriedade canônica PidNameXSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameXSharingFlavor
api_type:
- COM
ms.assetid: 7757fde1-564b-4f3a-9b9e-f80a143690ea
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bcdca783778e1a310be638ce376d408acf0b247f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580037"
---
# <a name="pidnamexsharingflavor-canonical-property"></a>Propriedade canônica PidNameXSharingFlavor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Representa o valor da propriedade **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).
  
|||
|:-----|:-----|
|Nomes amigáveis:  <br/> |Nenhum  <br/> |
|Propriedade definida:  <br/> |PS_INTERNET_HEADERS  <br/> |
|Nome da propriedade:  <br/> |Tipo de compartilhamento X  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Sharing  <br/> |
   
## <a name="remarks"></a>Comentários

A propriedade **dispidSharingFlavor** deve ser um dos seguintes valores. 
  
|**Valor**|**Tipo de mensagem de compartilhamento**|
|:-----|:-----|
|0x00020310  <br/> |Um convite de compartilhamento para uma pasta especial.  <br/> |
|0x00000310  <br/> |Um convite de compartilhamento para uma pasta que não é uma pasta especial.  <br/> |
|0x00020500  <br/> |Uma solicitação de compartilhamento.  <br/> |
|0x00020710  <br/> |Ambos os um convite de compartilhamento para uma pasta especial e uma solicitação de compartilhamento de pasta especial do equivalente do destinatário.  <br/> |
|0x00025100  <br/> |Uma resposta de compartilhamento que nega uma solicitação.  <br/> |
|0x00023310  <br/> |Uma resposta de compartilhamento que aceita uma solicitação (também um tipo de convite de compartilhamento).  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Compartilha pastas de caixa de correio entre clientes.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

