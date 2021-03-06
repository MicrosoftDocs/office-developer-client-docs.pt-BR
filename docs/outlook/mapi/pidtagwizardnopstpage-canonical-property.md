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
ms.openlocfilehash: e816af2ce60b4c06ae14f720cf7c36d58468d09d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422884"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a>Propriedade canônica PidTagWizardNoPstPage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Essa propriedade conterá TRUE se o assistente de perfil for suprimir a página PST (armazenamento de mensagens pessoais).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_WIZARD_NO_PST_PAGE  <br/> |
|Identificador:  <br/> |0x6700  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Exchange Administrative  <br/> |
   
## <a name="remarks"></a>Comentários

Os provedores de serviços podem definir essa propriedade ao chamar uma função com base no protótipo de [função LAUNCHWIZARDENTRY.](launchwizardentry.md) Essa propriedade informa ao assistente de perfil que o provedor não deseja que a página PST seja exibida durante a caixa de diálogo do usuário. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

