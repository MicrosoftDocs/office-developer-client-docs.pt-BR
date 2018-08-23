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
ms.openlocfilehash: 6398acf71e62157cf5a6eb7e6caf22130fa9f9d0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568802"
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

O conteúdo da cadeia de caracteres binário é definido pela origem da mensagem. Se o conjunto em uma mensagem de saída, esta propriedade deve ser copiado em todos os relatórios gerados em resposta à mensagem.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

