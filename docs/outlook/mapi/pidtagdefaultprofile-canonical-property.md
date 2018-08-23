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
ms.openlocfilehash: a315f1564f2980ad16ce2ba3da2308960f7d4b88
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578889"
---
# <a name="pidtagdefaultprofile-canonical-property"></a>Propriedade canônica PidTagDefaultProfile

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Conterá TRUE se um perfil de usuário de mensagens é o perfil padrão MAPI.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DEFAULT_PROFILE  <br/> |
|Identificador:  <br/> |0x3D04  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade não é exibido como uma propriedade de qualquer objeto, mas apenas como uma coluna em uma tabela de perfil. Um aplicativo cliente pode usar o método [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) para designar o perfil padrão. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

