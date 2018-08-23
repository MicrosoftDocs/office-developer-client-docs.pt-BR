---
title: Propriedade canônica PidTagAttachEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7475eef15398081a30307e7b4a077a0700a6ba8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584195"
---
# <a name="pidtagattachencoding-canonical-property"></a>Propriedade canônica PidTagAttachEncoding

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um identificador de objeto ASN. 1 que especifica a codificação de um anexo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_ENCODING  <br/> |
|Identificador:  <br/> |0x3702  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade identifica o algoritmo usado para transformar os dados em um anexo.
  
 **Observação** Não devem ser confundidas os **PR_ATTACH_ENCODING** e as propriedades de **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). Eles não são combinados ou relacionados. **PR_ATTACH_TAG** identifica o aplicativo que gerou originalmente o anexo. "Objeto" tem um significado muito mais geral no identificador de objeto de termos e em x. 400, que na programação orientado a objetos. 
  
Identificadores de objeto do objeto identificador sintaxe e exemplo forem definidos no MAPIOID. Arquivo de cabeçalho H. Valores para **PR_ATTACH_ENCODING** não estão limitados àqueles definidos no MAPIOID. H. Por exemplo, arquivos de Macintosh anexados podem usar um identificador, como MacBinary. 
  
Para obter informações completas sobre esses identificadores de objeto, consulte a documentação sobre ASN. 1, X.208 e 209. O identificador de objeto é encontrado no elemento de referência do aplicativo do ambiente FTBP (arquivo transferir corpo parte). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
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

