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
ms.openlocfilehash: 649490f18bb1a14a7056b49fd846e893fba304bd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575207"
---
# <a name="pidtagrenderingposition-canonical-property"></a>Propriedade canônica PidTagRenderingPosition

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um deslocamento, em caracteres, a ser usado na renderização de um anexo dentro do texto da mensagem principal.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RENDERING_POSITION  <br/> |
|Identificador:  <br/> |0x370B  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Anexo MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Quando o deslocamento fornecido é -1 (0xFFFFFFFF), o anexo não é processado usando essa propriedade. Todos os valores que não seja de -1 indicam a posição dentro da propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) em que o anexo é a ser renderizado.
  
 **Observação** O caractere indicado por esta propriedade em **PR_BODY** é substituído pelo anexo. Geralmente esse caractere é um espaço, embora um caractere de espaço reservado especial também pode ser usado. 
  
Essa propriedade é expresso em caracteres. Em alguns conjuntos de caracteres isso não é equivalente à bytes. Aplicativos Unicode poderá computar a posição com base em caracteres de dois bytes. Aplicativos do conjunto de caracteres de Byte duplo (DBCS) devem examinar o texto até o valor dessa propriedade, como sua representação de caracteres varia entre um e dois bytes por caractere.
  
Essa propriedade não deve ser usada com o texto de formato Rich Text (RTF). A posição de renderização é indicada em RTF por uma sequência de escape chamada o espaço reservado do objeto attachment. Esta sequência consiste a cadeia de caracteres `\objattph` seguido de um único caractere, normalmente um espaço, que será substituído pela renderização de anexo. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
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

