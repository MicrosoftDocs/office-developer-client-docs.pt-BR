---
title: Propriedade canônica PidTagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: de2342ef4d3e9d06f198e06dc19c65b7b144624f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387906"
---
# <a name="pidtagstatus-canonical-property"></a>Propriedade canônica PidTagStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma bitmask de 32 bits dos sinalizadores que definem o status de uma pasta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_STATUS  <br/> |
|Identificador:  <br/> |0x360B  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contêiner MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade para pastas é semelhante à propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) para mensagens. Seus sinalizadores são fornecidos para o aplicativo cliente apenas e não afetam o armazenamento de mensagens. Os clientes podem usar ou ignorar essas configurações. O cliente também pode definir seus próprios valores para os bits podem ser definidos pelo cliente dessa propriedade.
  
Um ou mais dos seguintes sinalizadores podem ser definido para a máscara de bits:
  
FLDSTATUS_DELMARKED 
  
> A pasta é marcada para exclusão. O aplicativo cliente define esse sinalizador.
    
FLDSTATUS_HIDDEN 
  
> A pasta está oculta.
    
FLDSTATUS_HIGHLIGHTED 
  
> A pasta é realçada, por exemplo, a mostrada na ordem inversa vídeo.
    
FLDSTATUS_TAGGED 
  
> A pasta está marcada.
    
Provedores de armazenamento de mensagem definir essa propriedade em uma pasta para um ou mais desses valores e clientes interpretam o status conforme apropriado para seus aplicativos. Por exemplo, um cliente pode usar o status de pasta para diferenciar visualmente as pastas em uma tabela de hierarquia, exibindo pastas com o mesmo status da mesma maneira. Pastas realçadas possam ser exibidas nas pastas de vídeos, marcadas reversos pastas marcadas para exclusão podem ser exibidas com um ícone consistente e pastas ocultas podem estar oculta.
  
Bits 16 a 31 ("0x10000" por meio de "0x80000000") dessa propriedade estarão disponíveis para uso pelo aplicativo cliente IPM. Todos os outros bits são reservados para uso pelo MAPI; aqueles não definidos na lista anterior devem ser definidas inicialmente como zero e não foi alteradas.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
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

