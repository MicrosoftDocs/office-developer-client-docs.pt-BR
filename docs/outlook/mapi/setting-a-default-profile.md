---
title: Definindo um perfil padrão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f6bf8f88fa3e87ae619fa32d759fc182290998ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439811"
---
# <a name="setting-a-default-profile"></a>Definindo um perfil padrão

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O perfil padrão é o perfil que será usado se você não especificar explicitamente um na chamada para [MAPILogonEx](mapilogonex.md), definindo, em vez disso, o MAPI_USE_DEFAULT sinalizador.
  
 **Para estabelecer um perfil padrão**
  
1. Chame a [função MAPIAdminProfiles](mapiadminprofiles.md) para recuperar um ponteiro da interface **IProfAdmin.** 
    
2. Chame [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md). **SetDefaultProfile** define a **propriedade PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) para o novo perfil padrão e remove a configuração do perfil padrão anterior.
    

