---
title: Recuperar identidade principal e do provedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2a87e32fe21aa6fb1d9296c568a74da994c146bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770258"
---
# <a name="retrieving-primary-and-provider-identity"></a><span data-ttu-id="d4050-103">Recuperar identidade principal e do provedor</span><span class="sxs-lookup"><span data-stu-id="d4050-103">Retrieving Primary and Provider Identity</span></span>

  
  
<span data-ttu-id="d4050-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4050-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4050-105">Provedores de serviços, geralmente provedores de catálogo de endereços, tem a opção de fornecer uma identidade que pode ser usada para representar a sessão em uma variedade de situações.</span><span class="sxs-lookup"><span data-stu-id="d4050-105">Service providers, typically address book providers, have the option of supplying an identity that can be used to represent the session in a variety of situations.</span></span> <span data-ttu-id="d4050-106">Três propriedades descrevem a identidade de um provedor:</span><span class="sxs-lookup"><span data-stu-id="d4050-106">Three properties describe a provider's identity:</span></span>
  
- <span data-ttu-id="d4050-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d4050-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span> 
    
- <span data-ttu-id="d4050-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d4050-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span> 
    
- <span data-ttu-id="d4050-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d4050-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="d4050-110">Essas propriedades são definidas para o identificador de entrada, nome para exibição e a chave de pesquisa do objeto identidade correspondente, que normalmente é um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d4050-110">These properties are set to the entry identifier, display name, and search key of the corresponding identity object, which is typically a messaging user.</span></span> <span data-ttu-id="d4050-111">Provedores de forneçam de uma identidade também definir o sinalizador STATUS_PRIMARY_IDENTITY em suas propriedades **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d4050-111">Providers that supply an identity also set the STATUS_PRIMARY_IDENTITY flag in their **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="d4050-112">Dependendo das suas necessidades, você pode usar a identidade de um determinado provedor ou a identidade principal para a sessão.</span><span class="sxs-lookup"><span data-stu-id="d4050-112">Depending on your needs, you might use a particular provider's identity or the primary identity for the session.</span></span> <span data-ttu-id="d4050-113">Você pode usar a identidade de um provedor também para fins de exibição ou para recuperar as propriedades, como **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d4050-113">You can use a provider's identity also for display purposes or to retrieve properties, such as **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span></span> <span data-ttu-id="d4050-114">**PR_RESOURCE_PATH**, se definida, que contém o caminho para arquivos usados ou criado pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="d4050-114">**PR_RESOURCE_PATH**, if set, contains the path to files used or created by the provider.</span></span> <span data-ttu-id="d4050-115">Recupere a propriedade **PR_RESOURCE_PATH** para o provedor fornecendo a identidade principal quando você deseja localizar os arquivos que pertencem ao usuário da sessão.</span><span class="sxs-lookup"><span data-stu-id="d4050-115">Retrieve the **PR_RESOURCE_PATH** property for the provider supplying the primary identity when you want to locate files that pertain to the user of the session.</span></span> 
  
 <span data-ttu-id="d4050-116">**Para recuperar a identidade de um provedor específico**</span><span class="sxs-lookup"><span data-stu-id="d4050-116">**To retrieve the identity of a specific provider**</span></span>
  
1. <span data-ttu-id="d4050-117">Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="d4050-117">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="d4050-118">Construa uma restrição usando uma estrutura de [SPropertyRestriction](spropertyrestriction.md) para corresponder à coluna **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) com o nome do provedor especificado.</span><span class="sxs-lookup"><span data-stu-id="d4050-118">Build a restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match the **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) column with the name of the specified provider.</span></span> 
    
3. <span data-ttu-id="d4050-119">Chame [IMAPITable:: FindRow](imapitable-findrow.md) para localizar linha do provedor.</span><span class="sxs-lookup"><span data-stu-id="d4050-119">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the provider's row.</span></span> <span data-ttu-id="d4050-120">Identidade do provedor será armazenada na coluna **PR_IDENTITY_ENTRYID** , se ela existir.</span><span class="sxs-lookup"><span data-stu-id="d4050-120">The provider's identity will be stored in the **PR_IDENTITY_ENTRYID** column, if it exists.</span></span> 
    
 <span data-ttu-id="d4050-121">**Para recuperar a identidade principal para uma sessão**</span><span class="sxs-lookup"><span data-stu-id="d4050-121">**To retrieve the primary identity for a session**</span></span>
  
- <span data-ttu-id="d4050-122">Chame [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="d4050-122">Call [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="d4050-123">**QueryIdentity** baseia a identidade de sessão na existência do valor STATUS_PRIMARY_IDENTITY na coluna **PR_RESOURCE_FLAGS** para uma das linhas da tabela de status.</span><span class="sxs-lookup"><span data-stu-id="d4050-123">**QueryIdentity** bases session identity on the existence of the STATUS_PRIMARY_IDENTITY value in the **PR_RESOURCE_FLAGS** column for one of the rows in the status table.</span></span> <span data-ttu-id="d4050-124">Se nenhuma das linhas de status tiver esse valor definido, **QueryIdentity** atribui a identidade para o primeiro provedor de serviços que define as propriedades PR_IDENTITY três.</span><span class="sxs-lookup"><span data-stu-id="d4050-124">If none of the status rows have this value set, **QueryIdentity** assigns identity to the first service provider that sets the three PR_IDENTITY properties.</span></span> <span data-ttu-id="d4050-125">Se nenhum provedor de serviço fornece uma identidade, **QueryIdentity** retorna MAPI_W_NO_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="d4050-125">If no service provider supplies an identity, **QueryIdentity** returns MAPI_W_NO_SERVICE.</span></span> <span data-ttu-id="d4050-126">Quando isso acontece, você deverá criar uma cadeia de caracteres para representar um usuário genérico que pode servir como a identidade principal.</span><span class="sxs-lookup"><span data-stu-id="d4050-126">When this happens, you should create a character string to represent a generic user that can serve as the primary identity.</span></span> 
    
 <span data-ttu-id="d4050-127">**Para definir explicitamente a identidade principal para uma sessão**</span><span class="sxs-lookup"><span data-stu-id="d4050-127">**To explicitly set the primary identity for a session**</span></span>
  
- <span data-ttu-id="d4050-128">Chame [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="d4050-128">Call [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span></span> <span data-ttu-id="d4050-129">Passe o **MAPIUID** para o provedor de serviço de destino.</span><span class="sxs-lookup"><span data-stu-id="d4050-129">Pass the **MAPIUID** for the target service provider.</span></span> 
    

