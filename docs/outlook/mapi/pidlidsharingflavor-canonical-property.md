---
title: Propriedade canônica PidLidSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ad98be2a457a1f7152f428f4aae834848a3b0536
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564553"
---
# <a name="pidlidsharingflavor-canonical-property"></a>Propriedade canônica PidLidSharingFlavor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Designa como uma propriedade de uma mensagem de compartilhamento.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidSharingFlavor  <br/> |
|Propriedade definida:  <br/> |PSETID_Sharing  <br/> |
|ID de longo (LID):  <br/> |0x00008A18  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Sharing  <br/> |
   
## <a name="remarks"></a>Comentários

O valor dessa propriedade deve ser um destes procedimentos:
  
|**Valor**|**Tipo de objeto de mensagem de compartilhamento**|
|:-----|:-----|
|0x00020310  <br/> |Um convite de compartilhamento para uma pasta especial.  <br/> |
|0x00000310  <br/> |Um convite de compartilhamento para uma pasta que não é uma pasta especial.  <br/> |
|0x00020500  <br/> |Uma solicitação de compartilhamento.  <br/> |
|0x00020710  <br/> |Ambos os um convite de compartilhamento para uma pasta especial e uma solicitação de compartilhamento de pasta especial do equivalente do destinatário.  <br/> |
|0x00025100  <br/> |Uma resposta de compartilhamento a negação uma solicitação.  <br/> |
|0x00023310  <br/> |Uma resposta de compartilhamento aceitar uma solicitação (também um tipo de convite de compartilhamento).  <br/> |
   
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

