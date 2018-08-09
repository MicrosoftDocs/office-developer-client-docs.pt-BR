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
ms.openlocfilehash: 8c104af106a885f42f8063bcf5fb55d654f2688e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769399"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a>Propriedade canônica PidTagJunkAddRecipientsToSafeSendersList

  
  
**Aplica-se a**: Outlook 
  
Indica se ou não os destinatários de email a ser adicionado à lista de remetentes confiáveis.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_JUNK_ADD_RECIPS_TO_SSL  <br/> |
|Identificador:  <br/> |0x6103  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>Comentários

Se houver, essa propriedade deverá ser definida como 0 ou 1. Um valor de 1 indica que os destinatários de email devem ser adicionados à lista de remetentes confiáveis. Um valor 0 indica que os destinatários de email não são a ser adicionado à lista de remetentes confiáveis.
  
Se essa propriedade estiver presente com um valor de 1, os endereços SMTP os destinatários do email devem ser adicionados à cláusula de remetentes confiáveis da condição de regra do lixo eletrônico. Se essa propriedade for 0, nenhuma ação é necessária.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite a manipulação das listas de permitir/bloquear e a determinação das mensagens de lixo eletrônico.
    
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

