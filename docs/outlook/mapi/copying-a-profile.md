---
title: Copiando um perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 77c7853c07830804aaa044f08078d95785bcfda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766319"
---
# <a name="copying-a-profile"></a>Copiando um perfil

  
  
**Aplica-se a**: Outlook 
  
Uma maneira para criar um perfil é a cópia de um perfil existente e alterar os serviços de mensagem necessárias e os provedores de serviços. Copiar um perfil envolve o uso de um objeto de administração de perfil, fornecido pelo MAPI por meio da função [MAPIAdminProfiles](mapiadminprofiles.md) . 
  
 **Para copiar um perfil**
  
1. Chame **MAPIAdminProfiles** para recuperar um ponteiro de interface **IProfAdmin** . 
    
2. Chame [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para acessar a tabela de perfil. 
    
3. Construa uma restrição de propriedade com uma estrutura de [SPropertyRestriction](spropertyrestriction.md) para corresponder **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) com o nome do perfil a ser copiado. 
    
4. Chame [IMAPITable:: FindRow](imapitable-findrow.md) para localizar a linha apropriada na tabela de perfil. 
    
5. Chame [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passando o valor da coluna **PR_DISPLAY_NAME** como o parâmetro _lpszOldProfileName_ . 
    

