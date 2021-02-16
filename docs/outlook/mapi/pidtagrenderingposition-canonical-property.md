---
title: Propriedade canônica PidTagRenderingPosition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRenderingPosition
api_type:
- COM
ms.assetid: bce46687-17dc-4a3f-96be-303d8755158e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d463be4a14ecf478bdcbddc50b4ad9360829befc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355150"
---
# <a name="pidtagrenderingposition-canonical-property"></a>Propriedade canônica PidTagRenderingPosition

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um deslocamento, em caracteres, a ser usado na renderização de um anexo no texto da mensagem principal.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RENDERING_POSITION  <br/> |
|Identificador:  <br/> |0x370B  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Anexo MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Quando o deslocamento fornecido for -1 (0xFFFFFFFF), o anexo não será renderizado usando essa propriedade. Todos os valores diferentes de -1 indicam a posição dentro da propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) na qual o anexo deve ser renderizado.
  
 **Observação** O caractere indicado por essa propriedade **PR_BODY** é substituído pelo anexo. Normalmente, esse caractere é um espaço, embora um caractere de espaço reservado especial também possa ser usado. 
  
Essa propriedade é expressa em caracteres. Em alguns conjuntos de caracteres, isso não é equivalente a bytes. Aplicativos Unicode podem calcular a posição com base em caracteres de dois byte. Double-Byte DBCS (Conjunto de Caracteres) deve examinar o texto até esse valor de propriedade, porque sua representação de caractere varia entre um e dois bytes por caractere.
  
Essa propriedade não deve ser usada com texto RTF (Rich Text Format). A posição de renderização é indicada em RTF por uma sequência de escape chamada de espaço reservado para anexo de objeto. Essa sequência consiste na cadeia de caracteres seguida por um único caractere, normalmente um espaço, que será  `\objattph` substituído pela renderização do anexo. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
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

