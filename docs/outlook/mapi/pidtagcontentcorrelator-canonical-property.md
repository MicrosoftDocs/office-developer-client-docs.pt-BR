---
title: Propriedade canônica PidTagContentCorrelator
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCorrelator
api_type:
- HeaderDef
ms.assetid: 0bf78879-2f9f-4c29-b1f4-2f4882d8464d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 96e0e3152a70eb2913c4559afd99e25adff48ca9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438523"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a>Propriedade canônica PidTagContentCorrelator

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor que o remetente da mensagem pode usar para corresponder a um relatório com a mensagem original.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTENT_CORRELATOR  <br/> |
|Identificador:  <br/> |0x0007  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentários

O conteúdo da cadeia de caracteres binária é definido pelo originador da mensagem. Se for definida em uma mensagem de saída, essa propriedade deverá ser copiada para todos os relatórios gerados em resposta à mensagem.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

