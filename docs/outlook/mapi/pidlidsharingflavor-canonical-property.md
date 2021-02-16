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
ms.openlocfilehash: 21144af15e7a36f54af3032f735c391b3038305b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327479"
---
# <a name="pidlidsharingflavor-canonical-property"></a>Propriedade canônica PidLidSharingFlavor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Designa como uma propriedade de uma mensagem de compartilhamento.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidSharingFlavor  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Sharing  <br/> |
|Long ID (LID):  <br/> |0x00008A18  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Compartilhamento  <br/> |
   
## <a name="remarks"></a>Comentários

O valor dessa propriedade deve ser um dos seguintes:
  
|**Valor**|**Tipo de objeto Sharing Message**|
|:-----|:-----|
|0x00020310  <br/> |Um convite de compartilhamento para uma pasta especial.  <br/> |
|0x00000310  <br/> |Um convite de compartilhamento para uma pasta que não é uma pasta especial.  <br/> |
|0x00020500  <br/> |Uma solicitação de compartilhamento.  <br/> |
|0x00020710  <br/> |Um convite de compartilhamento para uma pasta especial e uma solicitação de compartilhamento para a pasta especial equivalente do destinatário.  <br/> |
|0x00025100  <br/> |Uma resposta de compartilhamento negando uma solicitação.  <br/> |
|0x00023310  <br/> |Uma resposta de compartilhamento aceitando uma solicitação (também um tipo de convite de compartilhamento).  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Compartilha pastas de caixa de correio entre clientes.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

