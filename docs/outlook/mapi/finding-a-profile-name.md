---
title: Localizar um nome de perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b4efdd8d8238d4bc7e89a1153b9be34c7af76355
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407918"
---
# <a name="finding-a-profile-name"></a>Localizar um nome de perfil

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Às vezes, os clientes precisam encontrar o nome do perfil que está sendo usado na sessão, o nome do perfil padrão ou o nome de um perfil alternativo instalado no computador.
  
Há algumas maneiras de recuperar o nome de um perfil durante uma sessão. Se você precisar encontrar o nome de um perfil que não seja necessariamente aquele que está sendo usado para a sessão, use o primeiro procedimento. Se você precisar encontrar o nome do perfil padrão, use o segundo procedimento. Se você precisar encontrar o nome do perfil atual da sessão, use o último procedimento. 
  
 **Para encontrar o nome de qualquer perfil**
  
1. Chame [MAPIAdminProfiles para](mapiadminprofiles.md) recuperar um ponteiro da interface **IProfAdmin.** 
    
2. Chame [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para acessar a tabela de perfil. 
    
3. Chame o método [IMAPITable::QueryRows](imapitable-queryrows.md) da tabela de perfil para recuperar todas as linhas na tabela e examinar cada uma delas para determinar se ela representa seu perfil de destino. 
    
 **Para encontrar o nome do perfil padrão**
  
1. Chame [MAPIAdminProfiles](mapiadminprofiles.md).
    
2. Chame [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para acessar a tabela de perfil. 
    
3. Crie uma restrição de propriedade com uma estrutura [SPropertyRestriction](spropertyrestriction.md) para corresponder **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) com o valor TRUE.
    
4. Chame [IMAPITable::FindRow](imapitable-findrow.md) para localizar a linha na tabela de perfil que representa o perfil padrão. A **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) contém o nome do perfil padrão.
    
 **Para encontrar o nome do perfil atual**
  
Para encontrar o nome do perfil atual, conclua uma das seguintes etapas:
  
- Supondo que você tenha a estrutura [MAPIUID](mapiuid.md) representando uma das seções do perfil atual, passe-a no parâmetro  _lpUID_ para [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md). Recupere a propriedade PR_PROFILE_NAME **(** [PidTagProfileName](pidtagprofilename-canonical-property.md)) da seção de perfil usando seu [método IMAPIProp::GetProps.](imapiprop-getprops.md) 
    
- Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status e encontrar a linha que tem sua coluna PR_RESOURCE_TYPE ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) definida como **MAPI_SUBSYSTEM.** A **PR_DISPLAY_NAME** coluna desta linha é o nome do perfil. Não use a tabela de status durante a inicialização porque bloqueia um aplicativo até que o spooler MAPI termine de inicializar todos os provedores de transporte. Isso pode prejudicar o desempenho. 
    

