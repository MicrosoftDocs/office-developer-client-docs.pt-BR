---
title: Propriedade canônica PidTagJunkAddRecipientsToSafeSendersList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3a87beaa3873b5ccb449e5b1497262bad5bf1497
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282365"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a>Propriedade canônica PidTagJunkAddRecipientsToSafeSendersList

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica se os destinatários de email devem ser adicionados à lista de remetentes confiáveis.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_JUNK_ADD_RECIPS_TO_SSL  <br/> |
|Identificador:  <br/> |0x6103  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>Comentários

Se presente, essa propriedade deve ser definida como 0 ou 1. Um valor 1 indica que os destinatários de email devem ser adicionados à lista de remetentes confiáveis. O valor 0 indica que os destinatários de email não devem ser adicionados à lista de remetentes confiáveis.
  
Se essa propriedade estiver presente com um valor de 1, os endereços SMTP dos destinatários de email devem ser adicionados à cláusula de remetentes confiáveis da condição de regra de lixo eletrônico. Se essa propriedade for 0, nenhuma ação será necessária.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite a manipulação de listas de permissões/bloqueios e a determinação de mensagens de lixo eletrônico.
    
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

