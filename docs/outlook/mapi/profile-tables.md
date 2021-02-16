---
title: Tabelas de Perfis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 15c07c05af82389bce697c300cd9b1d504e98736
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424347"
---
# <a name="profile-tables"></a>Tabelas de Perfis

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A tabela de perfil lista informações sobre todos os perfis associados a um aplicativo cliente específico. Há uma tabela de perfil para cada sessão, implementada pelo MAPI para uso por clientes. 
  
Os clientes acessam a tabela de perfil chamando o [método IProfAdmin::GetProfileTable.](iprofadmin-getprofiletable.md) 
  
A tabela de perfil é uma tabela estática. Perfis que foram marcados para exclusão não estão incluídos na tabela de perfil.
  
Assim como na maioria das implementações de tabela, se **GetProfileTable** for chamado e não houver perfis disponíveis para o cliente, a tabela será criada com zero linhas. 
  
As propriedades a seguir compom o conjunto de colunas necessário nas tabelas de perfil:
  
 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

