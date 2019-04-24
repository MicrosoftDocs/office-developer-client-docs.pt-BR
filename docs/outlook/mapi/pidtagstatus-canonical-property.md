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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278789"
---
# <a name="pidtagstatus-canonical-property"></a>Propriedade canônica PidTagStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um bitmask de 32 bits de sinalizadores que definem o status da pasta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_STATUS  <br/> |
|Identificador:  <br/> |0x360B  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contêiner MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade para Folders é análoga à propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) para mensagens. Seus sinalizadores são fornecidos apenas para o aplicativo cliente e não afetam o repositório de mensagens. Os clientes podem usar ou ignorar essas configurações. O cliente também pode definir seus próprios valores para os bits definíveis pelo cliente dessa propriedade.
  
Um ou mais dos seguintes sinalizadores podem ser definidos para a bitmask:
  
FLDSTATUS_DELMARKED 
  
> A pasta está marcada para exclusão. O aplicativo cliente define esse sinalizador.
    
FLDSTATUS_HIDDEN 
  
> A pasta está oculta.
    
FLDSTATUS_HIGHLIGHTED 
  
> A pasta é realçada, por exemplo, mostrada em vídeo inverso.
    
FLDSTATUS_TAGGED 
  
> A pasta está marcada.
    
Provedores de repositórios de mensagens defina essa propriedade em uma pasta como um ou mais desses valores e clientes interpretam o status conforme apropriado para seus aplicativos. Por exemplo, um cliente pode usar o status da pasta para diferenciar visualmente entre pastas em uma tabela de hierarquia, exibindo pastas com o mesmo status da mesma maneira. Pastas reAlçadas podem ser mostradas no vídeo inverso, pastas marcadas e pastas marcadas para exclusão podem ser exibidas com um ícone significativo e pastas ocultas podem ser ocultadas.
  
Os bits 16 a 31 ("0x10000" por meio de "0x80000000") dessa propriedade estão disponíveis para uso pelo aplicativo cliente IPM. Todos os outros bits são reservados para uso por MAPI; os não definidos na lista anterior devem ser inicialmente definidos como zero e não alterados.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Manipula objetos Message e Attachment.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

