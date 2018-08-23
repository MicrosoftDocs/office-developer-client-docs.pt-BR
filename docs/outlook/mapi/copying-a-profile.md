---
title: Copiar um perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 53b7099ae74828a97eb703b865ba30ab385e9a5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564931"
---
# <a name="copying-a-profile"></a>Copiar um perfil

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma maneira para criar um perfil é a cópia de um perfil existente e alterar os serviços de mensagem necessárias e os provedores de serviços. Copiar um perfil envolve o uso de um objeto de administração de perfil, fornecido pelo MAPI por meio da função [MAPIAdminProfiles](mapiadminprofiles.md) . 
  
 **Para copiar um perfil**
  
1. Chame **MAPIAdminProfiles** para recuperar um ponteiro de interface **IProfAdmin** . 
    
2. Chame [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para acessar a tabela de perfil. 
    
3. Construa uma restrição de propriedade com uma estrutura de [SPropertyRestriction](spropertyrestriction.md) para corresponder **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) com o nome do perfil a ser copiado. 
    
4. Chame [IMAPITable:: FindRow](imapitable-findrow.md) para localizar a linha apropriada na tabela de perfil. 
    
5. Chame [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passando o valor da coluna **PR_DISPLAY_NAME** como o parâmetro _lpszOldProfileName_ . 
    

