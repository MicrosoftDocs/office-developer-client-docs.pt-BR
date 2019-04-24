---
title: Tabelas de perfis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 15c07c05af82389bce697c300cd9b1d504e98736
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328557"
---
# <a name="profile-tables"></a>Tabelas de perfis

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A tabela de perfis lista informações sobre todos os perfis associados a um aplicativo cliente específico. Há uma tabela de perfil para cada sessão, implementada pelo MAPI para uso por clientes. 
  
Os clientes acessam a tabela de perfis chamando o método [IProfAdmin::](iprofadmin-getprofiletable.md) getprofiletable. 
  
A tabela de perfil é uma tabela estática. Os perfis marcados para exclusão não estão incluídos na tabela de perfis.
  
Assim como ocorre com a maioria das **** implementações de tabelas, se getprofiletable é chamado e não há perfis disponíveis para o cliente, a tabela é criada com zero linhas. 
  
As propriedades a seguir compõem o conjunto de colunas necessárias nas tabelas de perfis:
  
 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

