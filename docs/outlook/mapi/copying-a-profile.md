---
title: Copiando um perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 86f381eff1dab0144afe0f94dcd6dd54d1ad7fa8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424725"
---
# <a name="copying-a-profile"></a>Copiando um perfil

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma maneira de criar um perfil é copiar de um perfil existente e alterar os serviços de mensagens e provedores de serviços de mensagens necessários. Copiar um perfil envolve o uso de um objeto de administração de perfil, fornecido por MAPI por meio da função [MAPIAdminProfiles.](mapiadminprofiles.md) 
  
 **Para copiar um perfil**
  
1. Chame **MAPIAdminProfiles para** recuperar um ponteiro da interface **IProfAdmin.** 
    
2. Chame [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para acessar a tabela de perfil. 
    
3. Crie uma restrição de propriedade com uma estrutura [SPropertyRestriction](spropertyrestriction.md) para corresponder **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) com o nome do perfil a ser copiado. 
    
4. Chame [IMAPITable::FindRow](imapitable-findrow.md) para localizar a linha apropriada na tabela de perfil. 
    
5. Chame [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passando o valor da coluna **PR_DISPLAY_NAME** como o _parâmetro lpszOldProfileName._ 
    

