---
title: Tabelas de perfis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1046c8d92feec16428329636257ed9c1f0ec8719
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571476"
---
# <a name="profile-tables"></a>Tabelas de perfis

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A tabela de perfil lista informações sobre todos os perfis associados com um aplicativo cliente específico. Há uma tabela de perfil para cada sessão, implementadas pelo MAPI para uso por clientes. 
  
Os clientes de acessar a tabela de perfil chamando o método [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) . 
  
A tabela de perfil é uma tabela estática. Perfis que foram marcados para exclusão não são incluídos na tabela de perfil.
  
Como com a maioria das implementações de tabela, se **GetProfileTable** é chamado e não existem perfis disponíveis para o cliente, a tabela é criada com zero linhas. 
  
As seguintes propriedades compõem a coluna necessária definida nas tabelas de perfil:
  
 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

