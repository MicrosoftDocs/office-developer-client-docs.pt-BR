---
title: Configurar um perfil padrão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2044969cc79990c9f0325fc7934e3426015fdc72
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591769"
---
# <a name="setting-a-default-profile"></a>Configurar um perfil padrão

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O perfil padrão será o que é usado se você não especificar explicitamente um na chamada a [MAPILogonEx](mapilogonex.md), em vez disso, definindo o sinalizador MAPI_USE_DEFAULT.
  
 **Para estabelecer um perfil padrão**
  
1. Chame a função [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar um ponteiro de interface **IProfAdmin** . 
    
2. Chame [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md). **SetDefaultProfile** define a propriedade **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) para o novo perfil padrão e remove a configuração de perfil padrão anterior.
    

