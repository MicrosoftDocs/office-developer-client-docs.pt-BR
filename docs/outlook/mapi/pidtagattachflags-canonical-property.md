---
title: Propriedade canônica PidTagAttachFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: efccd75cce04e4e392a7fbd9feecc7c8b49ab57e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339330"
---
# <a name="pidtagattachflags-canonical-property"></a>Propriedade canônica PidTagAttachFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma máscara de bits de sinalizadores para um anexo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_FLAGS  <br/> |
|Identificador:  <br/> |0x3714  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada para suporte a MHTML. 
  
Um ou mais dos sinalizadores a seguir podem ser definidos para a **PR_ATTACH_FLAGS** bitmask: 
  
ATT_INVISIBLE_IN_HTML 
  
> Indica que esse anexo não está disponível para aplicativos de renderização HTML e deve ser ignorado no processamento MIME (Multipurpose Internet Mail Extensions). 
    
ATT_INVISIBLE_IN_RTF 
  
> Indica que esse anexo não está disponível para aplicativos renderização em RTF (Rich Text Format) e deve ser ignorado pelo MAPI.
    
Se a **PR_ATTACH_FLAGS** propriedade for zero ou ausente, o anexo será processado por todos os aplicativos. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

