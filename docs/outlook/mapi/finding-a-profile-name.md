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
  
Os clientes às vezes precisam encontrar o nome do perfil que está sendo usado no momento para a sessão, o nome do perfil padrão ou o nome de um perfil alternativo instalado no computador.
  
Há algumas maneiras de recuperar o nome de um perfil durante o curso de uma sessão. Se você precisar localizar o nome de um perfil que não é necessariamente o que está sendo usado para a sessão, use o primeiro procedimento. Se você precisar localizar o nome do perfil padrão, use o segundo procedimento. Se você precisar localizar o nome do perfil atual da sessão, use o último procedimento. 
  
 **Para localizar o nome de qualquer perfil**
  
1. Chame [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar um ponteiro de interface **IProfAdmin** . 
    
2. Chame [IProfAdmin::](iprofadmin-getprofiletable.md) getprofiletable para acessar a tabela de perfil. 
    
3. Chame o método imApitable da tabela de perfil [:: QueryRows](imapitable-queryrows.md) para recuperar todas as linhas da tabela e examinar cada uma para determinar se ele representa o perfil de destino. 
    
 **Para localizar o nome do perfil padrão**
  
1. Chamar [MAPIAdminProfiles](mapiadminprofiles.md).
    
2. Chame [IProfAdmin::](iprofadmin-getprofiletable.md) getprofiletable para acessar a tabela de perfil. 
    
3. Criar uma restrição de propriedade com uma estrutura [SPropertyRestriction](spropertyrestriction.md) para corresponder a **PR_DEFAULT_PROFILE** ([PIDTAGDEFAULTPROFILE](pidtagdefaultprofile-canonical-property.md)) com o valor true.
    
4. Call [IMAPITable:: FindRow](imapitable-findrow.md) para localizar a linha na tabela de perfil que representa o perfil padrão. A coluna **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) contém o nome do perfil padrão.
    
 **Para localizar o nome do perfil atual**
  
Para localizar o nome do perfil atual, conclua uma das seguintes etapas:
  
- Supondo que você tenha a estrutura [MAPIUID](mapiuid.md) que representa uma das seções do perfil atual, passe-a no parâmetro _lpUID_ para [IMAPISession:: OpenProfileSection](imapisession-openprofilesection.md). Recupere a propriedade **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) da seção de perfil usando seu método [IMAPIProp::](imapiprop-getprops.md) GetProps. 
    
- Chame [IMAPISession::](imapisession-getstatustable.md) getstatustable para acessar a tabela de status e localize a linha que tem sua coluna **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) definida como MAPI_SUBSYSTEM. A coluna **PR_DISPLAY_NAME** dessa linha é o nome do perfil. Não use a tabela status durante a inicialização, pois ela bloqueia um aplicativo até que o spooler MAPI tenha concluído a inicialização de todos os provedores de transporte. Isso pode degradar seu desempenho. 
    

