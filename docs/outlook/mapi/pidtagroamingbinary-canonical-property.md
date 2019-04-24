---
title: Propriedade canônica PidTagRoamingBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ead7c9c33c92240ba5e458b68635b766caaa9760
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359560"
---
# <a name="pidtagroamingbinary-canonical-property"></a>Propriedade canônica PidTagRoamingBinary

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um fluxo de mensagens associado a uma subclasse de **IPM. **Classe de configuração. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ROAMING_BINARYSTREAM  <br/> |
|Identificador:  <br/> |0x7C09  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Configuração  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade contém o fluxo de dados associado a um **IPM. **Mensagem de classe da mensagem de configuração. O formato do fluxo depende da classe da mensagem. Por exemplo, uma mensagem de tipo de classe **IPM. A configuração. AutoComplete** será formatada como um [fluxo de preenchimento automático](autocomplete-stream.md).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências para as especificações de protocolo do Microsoft Exchange Server relacionadas.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Especifica o local e as propriedades dos dados de configuração de cliente e de servidor, como listas de categorias compartilhadas e horários de trabalho.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

