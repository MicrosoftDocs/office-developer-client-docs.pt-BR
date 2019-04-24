---
title: Abrir entradas do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6ebd6009700742e9b1159bc95ff0496c423e512c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326324"
---
# <a name="opening-address-book-entries"></a><span data-ttu-id="dd9e8-103">Abrir entradas do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="dd9e8-103">Opening address book entries</span></span>

<span data-ttu-id="dd9e8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd9e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd9e8-105">Quando um cliente ou provedor solicitar que um de seus objetos seja aberto, o MAPI chamará o método [IABLogon:: OpenEntry](iablogon-openentry.md) do provedor.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-105">When a client or provider has requested that one of your objects be opened, MAPI calls your provider's [IABLogon::OpenEntry](iablogon-openentry.md) method.</span></span> <span data-ttu-id="dd9e8-106">O MAPI determina que o identificador de entrada que representa o objeto de destino pertence ao seu provedor examinando a parte [MAPIUID](mapiuid.md) do identificador de entrada e fazendo a correspondência com o **MAPIUID** que seu provedor registrou na chamada para \*\* IMAPISupport:: SetProviderUID\*\*.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-106">MAPI determines that the entry identifier representing the target object belongs to your provider by examining the [MAPIUID](mapiuid.md) portion of the entry identifier and matching it to the **MAPIUID** that your provider registered in the call to **IMAPISupport::SetProviderUID**.</span></span> <span data-ttu-id="dd9e8-107">Em seguida, o MAPI chama o método **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="dd9e8-107">MAPI then calls your **OpenEntry** method.</span></span> <span data-ttu-id="dd9e8-108">Seu provedor deve responder recuperando o objeto correspondente — um contêiner, uma lista de distribuição ou um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-108">Your provider must respond by retrieving the corresponding object — a container, distribution list, or messaging user.</span></span> 
  
<span data-ttu-id="dd9e8-109">Um identificador de entrada nulo indica uma solicitação para abrir o contêiner raiz do provedor do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-109">A NULL entry identifier indicates a request to open the address book provider's root container.</span></span> <span data-ttu-id="dd9e8-110">Os clientes abrem o contêiner raiz para acessar sua tabela de hierarquia e seus destinatários.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-110">Clients open the root container to access its hierarchy table and its recipients.</span></span> <span data-ttu-id="dd9e8-111">Os provedores de catálogo de endereços que só fornecem modelos para a criação de destinatários únicos não oferecem suporte à chamada **OpenEntry** para o contêiner raiz.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-111">Address book providers that only supply templates for creating one-off recipients do not support the **OpenEntry** call for the root container.</span></span> 
  
### <a name="to-implement-iablogonopenentry"></a><span data-ttu-id="dd9e8-112">Para implementar o IABLogon:: OpenEntry</span><span class="sxs-lookup"><span data-stu-id="dd9e8-112">To implement IABLogon::OpenEntry</span></span>
  
1. <span data-ttu-id="dd9e8-113">Verifique se o identificador de entrada é um identificador válido para o qual seu provedor oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-113">Check that the entry identifier is a valid identifier that your provider supports.</span></span> <span data-ttu-id="dd9e8-114">Se não for um identificador de entrada válido, retorne MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-114">If it is not a valid entry identifier, return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="dd9e8-115">Verifique o sinalizador que é passado com o parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="dd9e8-115">Check the flag that is passed in with the  _ulFlags_ parameter.</span></span> <span data-ttu-id="dd9e8-116">Se o MAPI tiver passado no MAPI_MODIFY e seu provedor não permitir que seus objetos sejam modificados, falhará e retornará o valor de erro MAPI_E_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-116">If MAPI has passed in MAPI_MODIFY and your provider does not allow its objects to be modified, fail and return the MAPI_E_ACCESS_DENIED error value.</span></span> 
    
3. <span data-ttu-id="dd9e8-117">Verifique se a interface solicitada no parâmetro _lpInterface_ é válida para o tipo de objeto que seu provedor foi solicitado a abrir.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-117">Check that the interface requested in the  _lpInterface_ parameter is valid for the type of object your provider has been asked to open.</span></span> <span data-ttu-id="dd9e8-118">Se um parâmetro inválido tiver sido passado, falhar e retornar o valor de erro MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-118">If an invalid parameter has been passed in, fail and return the MAPI_E_INTERFACE_NOT_SUPPORTED error value.</span></span> 
    
4. <span data-ttu-id="dd9e8-119">Se o parâmetro _cbEntryID_ for zero, esta é uma solicitação para abrir o contêiner raiz do provedor.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-119">If the  _cbEntryID_ parameter is zero, this is a request to open your provider's root container.</span></span> <span data-ttu-id="dd9e8-120">Crie o contêiner raiz e retorne um ponteiro para sua implementação de interface **IABContainer** .</span><span class="sxs-lookup"><span data-stu-id="dd9e8-120">Create the root container and return a pointer to its **IABContainer** interface implementation.</span></span> 
    
5. <span data-ttu-id="dd9e8-121">Se seu provedor implementar vários objetos de logon, cada um com seu próprio **MAPIUID**registrado, mapeie o **MAPIUID** contido no identificador de entrada com o objeto de logon apropriado.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-121">If your provider implements several logon objects, each with its own registered **MAPIUID**, map the **MAPIUID** contained in the entry identifier with the appropriate logon object.</span></span> 
    
6. <span data-ttu-id="dd9e8-122">Determine qual tipo de objeto o identificador de entrada representa: um usuário de mensagens, uma lista de distribuição ou um contêiner pertencente ao seu provedor ou um usuário de mensagens única ou uma lista de distribuição para que o valor apropriado possa ser definido para o _lpulObjectType_ Construtor.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-122">Determine which type of object the entry identifier represents: a messaging user, distribution list, or container belonging to your provider or a one-off messaging user or distribution list so that the appropriate value can be set for the  _lpulObjectType_ parameter.</span></span> 
    
7. <span data-ttu-id="dd9e8-123">Crie o objeto do tipo apropriado e defina as seguintes propriedades básicas:</span><span class="sxs-lookup"><span data-stu-id="dd9e8-123">Create the object of the appropriate type and set the following basic properties:</span></span>
    
    - <span data-ttu-id="dd9e8-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dd9e8-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    - <span data-ttu-id="dd9e8-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dd9e8-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    - <span data-ttu-id="dd9e8-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dd9e8-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    - <span data-ttu-id="dd9e8-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dd9e8-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
8. <span data-ttu-id="dd9e8-128">Calcule **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) e **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de informações no identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-128">Calculate **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from information in the entry identifier.</span></span>
    
9. <span data-ttu-id="dd9e8-129">ReTorne um ponteiro para a implementação de interface para o objeto.</span><span class="sxs-lookup"><span data-stu-id="dd9e8-129">Return a pointer to the interface implementation for the object.</span></span> 
    

