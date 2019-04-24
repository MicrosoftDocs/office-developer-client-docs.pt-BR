---
title: Copiar um perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 86f381eff1dab0144afe0f94dcd6dd54d1ad7fa8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285227"
---
# <a name="copying-a-profile"></a>Copiar um perfil

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma maneira de criar um perfil é copiar de um perfil existente e alterar os serviços de mensagens e provedores de serviços necessários. Copiar um perfil envolve o uso de um objeto de administração de perfil, fornecido pelo MAPI através da função [MAPIAdminProfiles](mapiadminprofiles.md) . 
  
 **Para copiar um perfil**
  
1. Chame **MAPIAdminProfiles** para recuperar um ponteiro de interface **IProfAdmin** . 
    
2. Chame [IProfAdmin::](iprofadmin-getprofiletable.md) getprofiletable para acessar a tabela de perfil. 
    
3. Criar uma restrição de propriedade com uma estrutura [SPropertyRestriction](spropertyrestriction.md) para corresponder a **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) com o nome do perfil a ser copiado. 
    
4. Call [IMAPITable:: FindRow](imapitable-findrow.md) para localizar a linha apropriada na tabela de perfis. 
    
5. Chame [IProfAdmin:: CopyProfile](iprofadmin-copyprofile.md), passando o valor da coluna **PR_DISPLAY_NAME** como o parâmetro _lpszOldProfileName_ . 
    

