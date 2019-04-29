---
title: Propriedade canônica PidTagDefaultProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultProfile
api_type:
- HeaderDef
ms.assetid: 47f745a4-5a9c-42af-b076-a72548ef4d31
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8295ae6904f503ca831a00c1f35ac08596b5358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428771"
---
# <a name="pidtagdefaultprofile-canonical-property"></a>Propriedade canônica PidTagDefaultProfile

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém TRUE se um perfil de usuário de mensagens é o perfil padrão MAPI.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DEFAULT_PROFILE  <br/> |
|Identificador:  <br/> |0x3D04  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade não aparece como uma propriedade de qualquer objeto, mas somente como uma coluna em uma tabela de perfil. Um aplicativo cliente pode usar o método [IProfAdmin:: setdefaultprofile foi](iprofadmin-setdefaultprofile.md) para designar o perfil padrão. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

