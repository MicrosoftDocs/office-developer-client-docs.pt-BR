---
title: Propriedade canônica PidLidSharingResponseType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingResponseType
api_type:
- COM
ms.assetid: c27b1239-3612-4bb3-9f22-4b89ee9900cd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a645ee26b56355c6594f5667585becbcff2e3eec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768672"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a>Propriedade canônica PidLidSharingResponseType

  
  
**Aplica-se a**: Outlook 
  
Especifica o tipo de resposta com a qual o destinatário da solicitação de compartilhamento respondido. Esta é uma propriedade de uma mensagem de compartilhamento.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidSharingResponseType  <br/> |
|Propriedade definida:  <br/> |PSETID_Sharing  <br/> |
|ID de longo (LID):  <br/> |0x00008A27  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Sharing  <br/> |
   
## <a name="remarks"></a>Comentários

O valor dessa propriedade deve ser definido como um dos seguintes valores:
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0x00000000  <br/> |Nenhuma resposta  <br/> |
|0x00000001  <br/> |Aceito  <br/> |
|0x00000002  <br/> |Negado  <br/> |
   
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

