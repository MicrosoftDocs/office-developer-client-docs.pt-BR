---
title: Criar um perfil usando um código personalizado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f3270528194b3cc3429d3afec153355349dabbff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335785"
---
# <a name="creating-a-profile-by-using-custom-code"></a><span data-ttu-id="23b92-103">Criar um perfil usando um código personalizado</span><span class="sxs-lookup"><span data-stu-id="23b92-103">Creating a Profile by Using Custom Code</span></span>

  
  
<span data-ttu-id="23b92-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23b92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23b92-105">Se você optar por escrever código para criar um perfil, certifique-se de que você compreende como solicitar entradas de perfil e o tipo e a quantidade de informações necessárias para cada entrada.</span><span class="sxs-lookup"><span data-stu-id="23b92-105">If you choose to write code to create a profile, make sure that you understand how to order profile entries and the type and amount of information that is needed for each entry.</span></span> <span data-ttu-id="23b92-106">As implicações das entradas de ordenação em um perfil são explicadas em [perfis MAPI](mapi-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="23b92-106">The implications of ordering entries in a profile is explained in [MAPI Profiles](mapi-profiles.md).</span></span>
  
 <span data-ttu-id="23b92-107">**Para criar um perfil com código C ou C++**</span><span class="sxs-lookup"><span data-stu-id="23b92-107">**To create a profile with C or C++ code**</span></span>
  
1. <span data-ttu-id="23b92-108">Leia o arquivo de cabeçalho de cada serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="23b92-108">Read the header file for each message service.</span></span> <span data-ttu-id="23b92-109">Entenda quais propriedades você precisará configurar e quais valores você usará.</span><span class="sxs-lookup"><span data-stu-id="23b92-109">Understand what properties you will need to configure and what values you will use.</span></span>
    
2. <span data-ttu-id="23b92-110">Chame a função [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar um ponteiro de interface **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="23b92-110">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
3. <span data-ttu-id="23b92-111">Chame [IProfAdmin:: CreateProfile](iprofadmin-createprofile.md) para criar seu perfil.</span><span class="sxs-lookup"><span data-stu-id="23b92-111">Call [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) to create your profile.</span></span> <span data-ttu-id="23b92-112">Se você deseja criar um perfil com os serviços de mensagem listados na seção **[serviços padrão]** do MAPISVC. INF, defina o sinalizador MAPI_DEFAULT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="23b92-112">If you want to create a profile with the message services listed in the **[Default Services]** section of the MAPISVC.INF file, set the MAPI_DEFAULT_SERVICE flag.</span></span> <span data-ttu-id="23b92-113">Se você deseja permitir que o usuário insira informações de configuração, defina o sinalizador MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="23b92-113">If you want to enable the user to enter configuration information, set the MAPI_DIALOG flag.</span></span> <span data-ttu-id="23b92-114">Certifique-se de definir esse sinalizador se nem todas as informações necessárias estiverem disponíveis no MAPISVC. Arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="23b92-114">Make sure that you set this flag if not all of the necessary information is available through the MAPISVC.INF file.</span></span> <span data-ttu-id="23b92-115">**CreateProfile** chama a função de ponto de entrada para cada serviço de mensagens a ser adicionado ao perfil com MSG_SERVICE_CREATE definido como o parâmetro _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="23b92-115">**CreateProfile** calls the entry point function for each message service to be added to the profile with MSG_SERVICE_CREATE set as the  _ulContext_ parameter.</span></span> 
    
4. <span data-ttu-id="23b92-116">Chame [IProfAdmin:: adminservices](iprofadmin-adminservices.md) para obter um objeto de administração de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="23b92-116">Call [IProfAdmin::AdminServices](iprofadmin-adminservices.md) to obtain a message service administration object.</span></span> 
    
5. <span data-ttu-id="23b92-117">Use o objeto de administração do serviço de mensagens para adicionar serviços de mensagens ao perfil.</span><span class="sxs-lookup"><span data-stu-id="23b92-117">Use the message service administration object to add message services to the profile.</span></span> <span data-ttu-id="23b92-118">Para cada serviço de mensagens que você deseja adicionar:</span><span class="sxs-lookup"><span data-stu-id="23b92-118">For each message service that you want to add:</span></span>
    
1. <span data-ttu-id="23b92-119">Chame o método [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) para criar o novo serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="23b92-119">Call the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method to create the new message service.</span></span> 
    
2. <span data-ttu-id="23b92-120">Call [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passando a estrutura **MAPIUID** do serviço que você acabou de criar e uma matriz de valor de propriedade com suas propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="23b92-120">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passing the **MAPIUID** structure of the service you just created and a property value array with its configuration properties.</span></span> 
    
6. <span data-ttu-id="23b92-121">Para recuperar o identificador de um serviço recém-adicionado, que é sua propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), chame [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para acessar a tabela de serviço de mensagens e procure a linha que representa o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="23b92-121">To retrieve the identifier of a newly added service, which is its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property, call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to access the message service table and search for the row that represents the message service.</span></span> <span data-ttu-id="23b92-122">A última linha da tabela representará o serviço de mensagens mais recentemente adicionado.</span><span class="sxs-lookup"><span data-stu-id="23b92-122">The last row in the table will represent the most recently added message service.</span></span> 
    
<span data-ttu-id="23b92-123">Para tornar um novo perfil temporário, chame o método [IProfAdmin::D eleteprofile](iprofadmin-deleteprofile.md) imediatamente após o logon.</span><span class="sxs-lookup"><span data-stu-id="23b92-123">To make a new profile temporary, call the [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) method immediately after you log on.</span></span> <span data-ttu-id="23b92-124">O **DeleteProfile** irá marcar o novo perfil como excluído, ao torná-lo utilizável durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="23b92-124">**DeleteProfile** will mark the new profile as deleted while making it usable for the duration of the session.</span></span> <span data-ttu-id="23b92-125">Como ele não será incluído na tabela de perfis da sessão, outros clientes não poderão usá-lo.</span><span class="sxs-lookup"><span data-stu-id="23b92-125">Because it will not be included in the session's profile table, other clients will be unable to use it.</span></span> 
  

