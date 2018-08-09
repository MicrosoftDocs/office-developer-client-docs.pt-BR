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
ms.openlocfilehash: 84c2d02da840dfcad077462954cb10894ba153d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770178"
---
# <a name="profile-tables"></a>Tabelas de perfis

  
  
**Aplica-se a**: Outlook 
  
A tabela de perfil lista informações sobre todos os perfis associados com um aplicativo cliente específico. Há uma tabela de perfil para cada sessão, implementadas pelo MAPI para uso por clientes. 
  
Os clientes de acessar a tabela de perfil chamando o método [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) . 
  
A tabela de perfil é uma tabela estática. Perfis que foram marcados para exclusão não são incluídos na tabela de perfil.
  
Como com a maioria das implementações de tabela, se **GetProfileTable** é chamado e não existem perfis disponíveis para o cliente, a tabela é criada com zero linhas. 
  
As seguintes propriedades compõem a coluna necessária definida nas tabelas de perfil:
  
 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

