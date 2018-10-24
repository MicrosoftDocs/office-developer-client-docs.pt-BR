---
title: Localizar o nome de um perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a32c73f8a907b371c4d0f1c07050d44fd45801ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576285"
---
# <a name="finding-a-profile-name"></a>Localizar o nome de um perfil

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Às vezes, os clientes precisam encontrar o nome do perfil sendo utilizado para a sessão, o nome do perfil padrão ou o nome de um perfil alternativo instalado no computador.
  
Há algumas maneiras para recuperar o nome de um perfil durante o curso de uma sessão. Se você precisar encontrar o nome de um perfil que não é necessariamente aquele que está sendo usado para a sessão, use o procedimento primeiro. Se você precisar encontrar o nome do perfil padrão, use o procedimento segundo. Se você precisar encontrar o nome do perfil atual para a sessão, use o procedimento a último. 
  
 **Para localizar o nome de qualquer perfil**
  
1. Chame [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar um ponteiro de interface **IProfAdmin** . 
    
2. Chame [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para acessar a tabela de perfil. 
    
3. Chame o método de [IMAPITable:: QueryRows](imapitable-queryrows.md) da tabela perfil para recuperar todas as linhas na tabela e examinar cada um para determinar se ele representa seu perfil de destino. 
    
 **Para encontrar o nome do perfil padrão**
  
1. Chame [MAPIAdminProfiles](mapiadminprofiles.md).
    
2. Chame [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para acessar a tabela de perfil. 
    
3. Construa uma restrição de propriedade com uma estrutura de [SPropertyRestriction](spropertyrestriction.md) para corresponder **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) com o valor TRUE.
    
4. Chame [IMAPITable:: FindRow](imapitable-findrow.md) para localizar a linha na tabela de perfil que representa o perfil padrão. A coluna **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) contém o nome do perfil padrão.
    
 **Para encontrar o nome do perfil atual**
  
Para localizar o nome do perfil atual, conclua uma das seguintes etapas:
  
- Supondo que você tenha a estrutura [MAPIUID](mapiuid.md) que representa uma das seções do perfil atual, passe-o no parâmetro _lpUID_ para [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md). Recupere o perfil **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) a propriedade seção usando seu método [IMAPIProp::GetProps](imapiprop-getprops.md) . 
    
- Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status e localize a linha que tem uma coluna **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) definida como MAPI_SUBSYSTEM. A coluna **PR_DISPLAY_NAME** para essa linha é o nome do perfil. Não use a tabela de status durante o início do porque ele bloqueia um aplicativo até que o spooler MAPI concluiu Inicializando todos os provedores de transporte. Isso pode prejudicar o desempenho. 
    

