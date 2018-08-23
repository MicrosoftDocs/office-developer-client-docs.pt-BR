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
ms.openlocfilehash: cdb7dde4853188eb0621dc3c2f45c2dc713441d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570237"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a>Propriedade canônica PidTagWizardNoPabPage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Essa propriedade contém TRUE se o Assistente de perfil suprimir a página de catálogo (PAB) particular de endereços.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_WIZARD_NO_PAB_PAGE  <br/> |
|Identificador:  <br/> |0x6701  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Exchange administrativa  <br/> |
   
## <a name="remarks"></a>Comentários

Provedores de serviços podem definir essa propriedade, ao chamar uma função com base no protótipo de função [LAUNCHWIZARDENTRY](launchwizardentry.md) . Esta propriedade instrui o Assistente de perfil que o provedor não deseja que a página PAB sejam exibidas durante a caixa de diálogo do usuário. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

