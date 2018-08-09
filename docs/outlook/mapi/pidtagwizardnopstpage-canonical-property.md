---
title: Propriedade canônica PidTagWizardNoPstPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPstPage
api_type:
- COM
ms.assetid: 1ac09578-892b-4c72-92f6-c2419ac2efe8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b94e1f2d66f89d680cc738968342de0fbcee5cda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19770162"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a>Propriedade canônica PidTagWizardNoPstPage

  
  
**Aplica-se a**: Outlook 
  
Essa propriedade contém TRUE se o Assistente de perfil suprimir a página de repositório (. PST) da mensagem pessoal.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_WIZARD_NO_PST_PAGE  <br/> |
|Identificador:  <br/> |0x6700  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Exchange administrativa  <br/> |
   
## <a name="remarks"></a>Comentários

Provedores de serviços podem definir essa propriedade, ao chamar uma função com base no protótipo de função [LAUNCHWIZARDENTRY](launchwizardentry.md) . Esta propriedade instrui o Assistente de perfil que o provedor não deseja que a página de PST sejam exibidas durante a caixa de diálogo do usuário. 
  
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

