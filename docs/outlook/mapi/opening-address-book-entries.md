---
title: Entradas do catálogo de endereços de abertura
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c36c70eacffcb4a41af0e73eea85143ab737867f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768187"
---
# <a name="opening-address-book-entries"></a><span data-ttu-id="d3978-103">Entradas do catálogo de endereços de abertura</span><span class="sxs-lookup"><span data-stu-id="d3978-103">Opening address book entries</span></span>

<span data-ttu-id="d3978-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d3978-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d3978-105">Quando um cliente ou provedor solicitou que um dos seus objetos seja aberto, MAPI chama o método de [IABLogon::OpenEntry](iablogon-openentry.md) do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="d3978-105">When a client or provider has requested that one of your objects be opened, MAPI calls your provider's [IABLogon::OpenEntry](iablogon-openentry.md) method.</span></span> <span data-ttu-id="d3978-106">MAPI determina que o identificador de entrada que representa o objeto de destino pertence ao seu provedor examinando a parte [MAPIUID](mapiuid.md) do identificador de entrada e estabelecendo uma correspondência para o seu provedor registrado na chamada a ** **MAPIUID** IMAPISupport::SetProviderUID**.</span><span class="sxs-lookup"><span data-stu-id="d3978-106">MAPI determines that the entry identifier representing the target object belongs to your provider by examining the [MAPIUID](mapiuid.md) portion of the entry identifier and matching it to the **MAPIUID** that your provider registered in the call to **IMAPISupport::SetProviderUID**.</span></span> <span data-ttu-id="d3978-107">MAPI chama seu método **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="d3978-107">MAPI then calls your **OpenEntry** method.</span></span> <span data-ttu-id="d3978-108">Seu provedor deve responder recuperando o objeto correspondente — um contêiner, lista de distribuição ou mensagens de usuário.</span><span class="sxs-lookup"><span data-stu-id="d3978-108">Your provider must respond by retrieving the corresponding object — a container, distribution list, or messaging user.</span></span> 
  
<span data-ttu-id="d3978-109">Um identificador de entrada NULL indica uma solicitação para abrir o contêiner de raiz do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="d3978-109">A NULL entry identifier indicates a request to open the address book provider's root container.</span></span> <span data-ttu-id="d3978-110">Clientes abrem o contêiner de raiz para acessar sua tabela de hierarquia e seus destinatários.</span><span class="sxs-lookup"><span data-stu-id="d3978-110">Clients open the root container to access its hierarchy table and its recipients.</span></span> <span data-ttu-id="d3978-111">Provedores de catálogo de endereços que apenas forneçam modelos para criação de destinatários únicos não têm suporte para a chamada **OpenEntry** para o contêiner de raiz.</span><span class="sxs-lookup"><span data-stu-id="d3978-111">Address book providers that only supply templates for creating one-off recipients do not support the **OpenEntry** call for the root container.</span></span> 
  
### <a name="to-implement-iablogonopenentry"></a><span data-ttu-id="d3978-112">Para implementar IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="d3978-112">To implement IABLogon::OpenEntry</span></span>
  
1. <span data-ttu-id="d3978-113">Verifique se o identificador de entrada é um identificador válido que o provedor oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="d3978-113">Check that the entry identifier is a valid identifier that your provider supports.</span></span> <span data-ttu-id="d3978-114">Se ele não é um identificador de entrada válida, retorne MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="d3978-114">If it is not a valid entry identifier, return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="d3978-115">Verifique se o sinalizador que é passado com o parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="d3978-115">Check the flag that is passed in with the  _ulFlags_ parameter.</span></span> <span data-ttu-id="d3978-116">Se o MAPI passou no MAPI_MODIFY e seu provedor não permite que seus objetos a ser modificada, falhar e retornar o valor de erro MAPI_E_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="d3978-116">If MAPI has passed in MAPI_MODIFY and your provider does not allow its objects to be modified, fail and return the MAPI_E_ACCESS_DENIED error value.</span></span> 
    
3. <span data-ttu-id="d3978-117">Verifique se a interface solicitada no parâmetro _lpInterface_ é válida para o tipo de objeto que foi solicitado para abrir seu provedor.</span><span class="sxs-lookup"><span data-stu-id="d3978-117">Check that the interface requested in the  _lpInterface_ parameter is valid for the type of object your provider has been asked to open.</span></span> <span data-ttu-id="d3978-118">Se um parâmetro inválido foi passado na, falhar e retornar o valor de erro MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="d3978-118">If an invalid parameter has been passed in, fail and return the MAPI_E_INTERFACE_NOT_SUPPORTED error value.</span></span> 
    
4. <span data-ttu-id="d3978-119">Se o parâmetro _cbEntryID_ for zero, essa é uma solicitação para abrir o contêiner de raiz do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="d3978-119">If the  _cbEntryID_ parameter is zero, this is a request to open your provider's root container.</span></span> <span data-ttu-id="d3978-120">Criar o contêiner de raiz e retornar um ponteiro para sua implementação de interface **IABContainer** .</span><span class="sxs-lookup"><span data-stu-id="d3978-120">Create the root container and return a pointer to its **IABContainer** interface implementation.</span></span> 
    
5. <span data-ttu-id="d3978-121">Se seu provedor implementa vários objetos de logon, cada um com seu próprio registrado **MAPIUID**, mapa a **MAPIUID** contidos no identificador de entrada com o objeto de logon adequada.</span><span class="sxs-lookup"><span data-stu-id="d3978-121">If your provider implements several logon objects, each with its own registered **MAPIUID**, map the **MAPIUID** contained in the entry identifier with the appropriate logon object.</span></span> 
    
6. <span data-ttu-id="d3978-122">Determinar o identificador de entrada de qual tipo de objeto representa: um usuário, lista de distribuição ou contêiner pertencente ao seu provedor ou uma lista de distribuição ou usuário mensagens único para que o valor apropriado pode ser definido para o _lpulObjectType_ mensagens Use o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d3978-122">Determine which type of object the entry identifier represents: a messaging user, distribution list, or container belonging to your provider or a one-off messaging user or distribution list so that the appropriate value can be set for the  _lpulObjectType_ parameter.</span></span> 
    
7. <span data-ttu-id="d3978-123">Criar o objeto do tipo apropriado e defina as seguintes propriedades básicas:</span><span class="sxs-lookup"><span data-stu-id="d3978-123">Create the object of the appropriate type and set the following basic properties:</span></span>
    
    - <span data-ttu-id="d3978-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3978-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    - <span data-ttu-id="d3978-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3978-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    - <span data-ttu-id="d3978-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3978-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    - <span data-ttu-id="d3978-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3978-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
8. <span data-ttu-id="d3978-128">Calcule **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) e **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) das informações do identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="d3978-128">Calculate **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from information in the entry identifier.</span></span>
    
9. <span data-ttu-id="d3978-129">Retorne um ponteiro para a implementação de interface para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d3978-129">Return a pointer to the interface implementation for the object.</span></span> 
    

