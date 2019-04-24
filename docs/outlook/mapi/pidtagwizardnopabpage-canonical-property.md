---
title: Propriedade canônica PidTagWizardNoPabPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPabPage
api_type:
- COM
ms.assetid: 9cec22cd-798d-41f6-9ebd-c7354f2162c2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fc971be76dbaa83176f207411f9f125ffee386cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350649"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a>Propriedade canônica PidTagWizardNoPabPage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Essa propriedade contém TRUE se o assistente de perfil é para suprimir a página do catálogo de endereços pessoal (PAB).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_WIZARD_NO_PAB_PAGE  <br/> |
|Identificador:  <br/> |0x6701  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Administrativo do Exchange  <br/> |
   
## <a name="remarks"></a>Comentários

Os provedores de serviços podem definir essa propriedade ao chamar uma função com base no protótipo de função [LAUNCHWIZARDENTRY](launchwizardentry.md) . Essa propriedade informa ao assistente de perfil que o provedor não quer que a página do PAB seja exibida durante a caixa de diálogo do usuário. 
  
## <a name="related-resources"></a>Recursos relacionados

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

