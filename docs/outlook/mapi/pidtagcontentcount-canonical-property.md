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
ms.openlocfilehash: 7e9994da72bbc38a546f220e5ecf8768b80c6f1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331952"
---
# <a name="pidtagcontentcount-canonical-property"></a>Propriedade canônica PidTagContentCount

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o número de mensagens em uma pasta, conforme calculado pelo armazenamento de mensagens.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTENT_COUNT  <br/> |
|Identificador:  <br/> |0x3602  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade calculada pelo armazenamento de mensagens é usada para duas finalidades diferentes, porém relacionadas. Em um objeto MapiFolder, ele contém o número de mensagens em uma pasta. Em uma linha de título em tabelas MAPI categorizadas, ela contém o número de mensagens não associadas na categoria correspondente a essa linha de título.
  
O número contido nessa propriedade não inclui entradas associadas na pasta. **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contém a contagem de mensagens não lidas para a pasta. Um aplicativo cliente pode ler, mas não alterar essa propriedade **e PR_CONTENT_UNREAD**. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo do Microsoft Exchange Server relacionadas.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Lida com operações de pasta.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclui operações permitidas para os objetos de tabela principais.
    
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

