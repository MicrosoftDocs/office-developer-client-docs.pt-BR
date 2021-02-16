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
# <a name="finding-a-profile-name"></a><span data-ttu-id="1adf3-103">Localizar um nome de perfil</span><span class="sxs-lookup"><span data-stu-id="1adf3-103">Finding a Profile Name</span></span>

  
  
<span data-ttu-id="1adf3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1adf3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1adf3-105">Às vezes, os clientes precisam encontrar o nome do perfil que está sendo usado na sessão, o nome do perfil padrão ou o nome de um perfil alternativo instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="1adf3-105">Clients sometimes need to find the name of the profile currently being used for the session, the name of the default profile, or the name of an alternate profile installed on the computer.</span></span>
  
<span data-ttu-id="1adf3-106">Há algumas maneiras de recuperar o nome de um perfil durante uma sessão.</span><span class="sxs-lookup"><span data-stu-id="1adf3-106">There are a few ways to retrieve the name of a profile during the course of a session.</span></span> <span data-ttu-id="1adf3-107">Se você precisar encontrar o nome de um perfil que não seja necessariamente aquele que está sendo usado para a sessão, use o primeiro procedimento.</span><span class="sxs-lookup"><span data-stu-id="1adf3-107">If you need to find the name of a profile that is not necessarily the one being used for the session, use the first procedure.</span></span> <span data-ttu-id="1adf3-108">Se você precisar encontrar o nome do perfil padrão, use o segundo procedimento.</span><span class="sxs-lookup"><span data-stu-id="1adf3-108">If you need to find the name of the default profile, use the second procedure.</span></span> <span data-ttu-id="1adf3-109">Se você precisar encontrar o nome do perfil atual da sessão, use o último procedimento.</span><span class="sxs-lookup"><span data-stu-id="1adf3-109">If you need to find the name of the current profile for the session, use the last procedure.</span></span> 
  
 <span data-ttu-id="1adf3-110">**Para encontrar o nome de qualquer perfil**</span><span class="sxs-lookup"><span data-stu-id="1adf3-110">**To find the name of any profile**</span></span>
  
1. <span data-ttu-id="1adf3-111">Chame [MAPIAdminProfiles para](mapiadminprofiles.md) recuperar um ponteiro da interface **IProfAdmin.**</span><span class="sxs-lookup"><span data-stu-id="1adf3-111">Call [MAPIAdminProfiles](mapiadminprofiles.md) to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="1adf3-112">Chame [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para acessar a tabela de perfil.</span><span class="sxs-lookup"><span data-stu-id="1adf3-112">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="1adf3-113">Chame o método [IMAPITable::QueryRows](imapitable-queryrows.md) da tabela de perfil para recuperar todas as linhas na tabela e examinar cada uma delas para determinar se ela representa seu perfil de destino.</span><span class="sxs-lookup"><span data-stu-id="1adf3-113">Call the profile table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve all of the rows in the table and examine each one to determine if it represents your target profile.</span></span> 
    
 <span data-ttu-id="1adf3-114">**Para encontrar o nome do perfil padrão**</span><span class="sxs-lookup"><span data-stu-id="1adf3-114">**To find the name of the default profile**</span></span>
  
1. <span data-ttu-id="1adf3-115">Chame [MAPIAdminProfiles](mapiadminprofiles.md).</span><span class="sxs-lookup"><span data-stu-id="1adf3-115">Call [MAPIAdminProfiles](mapiadminprofiles.md).</span></span>
    
2. <span data-ttu-id="1adf3-116">Chame [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para acessar a tabela de perfil.</span><span class="sxs-lookup"><span data-stu-id="1adf3-116">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="1adf3-117">Crie uma restrição de propriedade com uma estrutura [SPropertyRestriction](spropertyrestriction.md) para corresponder **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) com o valor TRUE.</span><span class="sxs-lookup"><span data-stu-id="1adf3-117">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) with the value TRUE.</span></span>
    
4. <span data-ttu-id="1adf3-118">Chame [IMAPITable::FindRow](imapitable-findrow.md) para localizar a linha na tabela de perfil que representa o perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="1adf3-118">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the row in the profile table that represents the default profile.</span></span> <span data-ttu-id="1adf3-119">A **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) contém o nome do perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="1adf3-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column contains the name of the default profile.</span></span>
    
 <span data-ttu-id="1adf3-120">**Para encontrar o nome do perfil atual**</span><span class="sxs-lookup"><span data-stu-id="1adf3-120">**To find the name of the current profile**</span></span>
  
<span data-ttu-id="1adf3-121">Para encontrar o nome do perfil atual, conclua uma das seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="1adf3-121">To find the name of the current profile, complete one of the following steps:</span></span>
  
- <span data-ttu-id="1adf3-122">Supondo que você tenha a estrutura [MAPIUID](mapiuid.md) representando uma das seções do perfil atual, passe-a no parâmetro  _lpUID_ para [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span><span class="sxs-lookup"><span data-stu-id="1adf3-122">Assuming that you have the [MAPIUID](mapiuid.md) structure representing one of the current profile's sections, pass it in the  _lpUID_ parameter to [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span></span> <span data-ttu-id="1adf3-123">Recupere a propriedade PR_PROFILE_NAME **(** [PidTagProfileName](pidtagprofilename-canonical-property.md)) da seção de perfil usando seu [método IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="1adf3-123">Retrieve the profile section's **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property using its [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
    
- <span data-ttu-id="1adf3-124">Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status e encontrar a linha que tem sua coluna PR_RESOURCE_TYPE ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) definida como **MAPI_SUBSYSTEM.**</span><span class="sxs-lookup"><span data-stu-id="1adf3-124">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table and find the row that has its **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column set to MAPI_SUBSYSTEM.</span></span> <span data-ttu-id="1adf3-125">A **PR_DISPLAY_NAME** coluna desta linha é o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="1adf3-125">The **PR_DISPLAY_NAME** column for this row is the profile name.</span></span> <span data-ttu-id="1adf3-126">Não use a tabela de status durante a inicialização porque bloqueia um aplicativo até que o spooler MAPI termine de inicializar todos os provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="1adf3-126">Do not use the status table during start up because it blocks an application until the MAPI spooler has finished initializing all of the transport providers.</span></span> <span data-ttu-id="1adf3-127">Isso pode prejudicar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="1adf3-127">This can degrade your performance.</span></span> 
    

