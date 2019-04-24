---
title: ConFigurando um perfil padrão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f6bf8f88fa3e87ae619fa32d759fc182290998ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339304"
---
# <a name="setting-a-default-profile"></a>ConFigurando um perfil padrão

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O perfil padrão é o perfil que é usado se você não especificar explicitamente um na chamada para [funçãomapilogonex](mapilogonex.md), definindo, em vez disso, o sinalizador MAPI_USE_DEFAULT.
  
 **Para estabelecer um perfil padrão**
  
1. Chame a função [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar um ponteiro de interface **IProfAdmin** . 
    
2. Chamar [IProfAdmin:: setdefaultprofile foi](iprofadmin-setdefaultprofile.md). **Setdefaultprofile foi** define a propriedade **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) para o novo perfil padrão e remove a configuração do perfil padrão anterior.
    

