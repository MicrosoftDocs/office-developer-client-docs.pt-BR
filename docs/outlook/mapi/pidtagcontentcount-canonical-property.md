---
title: Propriedade canônica PidTagContentCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCount
api_type:
- HeaderDef
ms.assetid: 27c75031-a968-4636-98a6-4a5b7422f57c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3c542b07eac626da5fbbb6a96b4545ad3c8558b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769110"
---
# <a name="pidtagcontentcount-canonical-property"></a>Propriedade canônica PidTagContentCount

  
  
**Aplica-se a**: Outlook 
  
Contém o número de mensagens em uma pasta, como computado pelo armazenamento de mensagens.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTENT_COUNT  <br/> |
|Identificador:  <br/> |0x3602  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade computada pelo armazenamento de mensagens é usada para dois diferentes, embora relacionado, fins. Em um objeto MapiFolder, ele contém o número de mensagens em uma pasta. Em uma linha de cabeçalho nas tabelas MAPI categorizadas, ele contém o número de mensagens não associado na categoria correspondente para essa linha de título.
  
O número contido nessa propriedade não inclui entradas associadas na pasta. **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contém a contagem de mensagens não lidas da pasta. Um aplicativo cliente pode ler, mas não alterar essa propriedade e **PR_CONTENT_UNREAD**. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Microsoft Exchange Server.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Trata as operações de pasta.
    
[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclui as operações permitidas para os objetos de tabela principal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

