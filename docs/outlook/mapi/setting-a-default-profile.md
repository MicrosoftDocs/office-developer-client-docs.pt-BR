---
title: Configurar um perfil padrão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ea21e735dba8690a392629b92b636b834d7d57d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770372"
---
# <a name="setting-a-default-profile"></a>Configurar um perfil padrão

  
  
**Aplica-se a**: Outlook 
  
O perfil padrão será o que é usado se você não especificar explicitamente um na chamada a [MAPILogonEx](mapilogonex.md), em vez disso, definindo o sinalizador MAPI_USE_DEFAULT.
  
 **Para estabelecer um perfil padrão**
  
1. Chame a função [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar um ponteiro de interface **IProfAdmin** . 
    
2. Chame [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md). **SetDefaultProfile** define a propriedade **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) para o novo perfil padrão e remove a configuração de perfil padrão anterior.
    

