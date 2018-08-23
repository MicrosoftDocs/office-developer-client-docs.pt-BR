---
title: Registrar identificadores exclusivos do provedor de serviços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: bde7ff73f58c8809d2dd6467daea28461e7c6ef7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586267"
---
# <a name="registering-service-provider-unique-identifiers"></a><span data-ttu-id="5b78c-103">Registrar identificadores exclusivos do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="5b78c-103">Registering Service Provider Unique Identifiers</span></span>

  
  
<span data-ttu-id="5b78c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b78c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b78c-105">Catálogo de endereços, armazenamento de mensagens e provedores de transporte usam um identificador exclusivo, conhecido como um [MAPIUID](mapiuid.md) para registrar para objetos de vários tipos de serviço.</span><span class="sxs-lookup"><span data-stu-id="5b78c-105">Address book, message store, and transport providers use a unique identifier known as a [MAPIUID](mapiuid.md) to register to service objects of various types.</span></span> <span data-ttu-id="5b78c-106">Um **MAPIUID** é um identificador de 16 bytes que contenha um GUID.</span><span class="sxs-lookup"><span data-stu-id="5b78c-106">A **MAPIUID** is a 16-byte identifier that contains a GUID.</span></span> <span data-ttu-id="5b78c-107">Você pode criar um **MAPIUID** usando o procedimento a seguir:</span><span class="sxs-lookup"><span data-stu-id="5b78c-107">You can create a **MAPIUID** by using the following procedure:</span></span> 
  
1. <span data-ttu-id="5b78c-108">Defina uma constante.</span><span class="sxs-lookup"><span data-stu-id="5b78c-108">Define a constant.</span></span>
    
2. <span data-ttu-id="5b78c-109">Invocar o Visual Studio*Criar GUID*\* ferramenta.</span><span class="sxs-lookup"><span data-stu-id="5b78c-109">Invoke the Visual Studio*Create GUID*\* tool.</span></span> 
    
<span data-ttu-id="5b78c-110">Por exemplo, um provedor de catálogo de endereços pode incluir a seguinte constante em um arquivo de cabeçalho para definir um **MAPIUID**:</span><span class="sxs-lookup"><span data-stu-id="5b78c-110">For example, an address book provider might include the following constant in a header file to define a **MAPIUID**:</span></span>
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 <span data-ttu-id="5b78c-111">**Para registrar um MAPIUID se seu provedor for um provedor de repositório de catálogo ou mensagem de endereço**</span><span class="sxs-lookup"><span data-stu-id="5b78c-111">**To register a MAPIUID if your provider is an address book or message store provider**</span></span>
  
1. <span data-ttu-id="5b78c-112">Chame [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="5b78c-112">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
    
2. <span data-ttu-id="5b78c-113">Registrar um **MAPIUID** para cada logon do objeto que você instancia e incluir este **MAPIUID** nos primeiros 16 bytes do membro de cada identificador de entrada que você criar **ab** .</span><span class="sxs-lookup"><span data-stu-id="5b78c-113">Register a **MAPIUID** for each logon object that you instantiate and include this **MAPIUID** in the first 16 bytes of the **ab** member of every entry identifier that you create.</span></span> <span data-ttu-id="5b78c-114">MAPI usa estruturas **MAPIUID** para associar objetos de provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="5b78c-114">MAPI uses **MAPIUID** structures to associate objects with service providers.</span></span> <span data-ttu-id="5b78c-115">Quando a chamadas de cliente que o método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir um objeto, MAPI examina a parte **MAPIUID** do identificador de entrada, estabelecendo uma correspondência contra o registrados **MAPIUID**, para determinar qual objeto logon deve receber a abrir solicitação.</span><span class="sxs-lookup"><span data-stu-id="5b78c-115">When a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open an object, MAPI examines the **MAPIUID** portion of the entry identifier, matching it against the registered **MAPIUID**, to determine which logon object should receive the open request.</span></span>
    
3. <span data-ttu-id="5b78c-116">Se seu provedor for um transporte, registre uma ou mais estruturas **MAPIUID** quando seu método de **IXPLogon::AddressTypes** chamadas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="5b78c-116">If your provider is a transport, register one or more **MAPIUID** structures when MAPI calls your **IXPLogon::AddressTypes** method.</span></span> <span data-ttu-id="5b78c-117">MAPI usa as estruturas **MAPIUID** registradas por provedores de transporte para atribuir a responsabilidade de entrega da mensagem.</span><span class="sxs-lookup"><span data-stu-id="5b78c-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span></span> 
    
<span data-ttu-id="5b78c-118">Embora os provedores de serviço geralmente registrar um único **MAPIUID**, você pode registrar várias estruturas de **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="5b78c-118">Although service providers typically register a single **MAPIUID**, you can register multiple **MAPIUID** structures.</span></span> <span data-ttu-id="5b78c-119">Se seu catálogo de endereços ou mensagem armazenar provedor suporta vários objetos de logon, talvez, permitindo que um usuário para adicionar mais de uma instância do provedor de ao seu perfil, você talvez queira implementar um **MAPIUID** de diferentes para cada objeto de logon.</span><span class="sxs-lookup"><span data-stu-id="5b78c-119">If your address book or message store provider supports multiple logon objects, perhaps by permitting a user to add more than one instance of your provider to their profile, you might want to implement a different **MAPIUID** for each logon object.</span></span> <span data-ttu-id="5b78c-120">Existem alguns outros motivos para dar suporte a mais de um **MAPIUID**:</span><span class="sxs-lookup"><span data-stu-id="5b78c-120">There are a few other reasons to support more than one **MAPIUID**:</span></span>
  
- <span data-ttu-id="5b78c-121">Você deve oferecer suporte a mais de uma versão do seu provedor e os identificadores de entrada devem representam a versão apropriada.</span><span class="sxs-lookup"><span data-stu-id="5b78c-121">You must support more than one version of your provider and the entry identifiers must represent the appropriate version.</span></span> <span data-ttu-id="5b78c-122">Atribua um **MAPIUID** de diferentes para cada versão.</span><span class="sxs-lookup"><span data-stu-id="5b78c-122">Assign a different **MAPIUID** for each version.</span></span> 
    
- <span data-ttu-id="5b78c-123">Você deseja distinguir entre os tipos de objetos que você ofereça suporte.</span><span class="sxs-lookup"><span data-stu-id="5b78c-123">You want to distinguish between the types of objects you support.</span></span> <span data-ttu-id="5b78c-124">Por exemplo, um provedor de catálogo de endereços talvez queira registrar um **MAPIUID** para usar os identificadores de entrada dos seus objetos de usuário de mensagens e um **MAPIUID** diferente a ser usado para listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="5b78c-124">For example, an address book provider might want to register one **MAPIUID** to use in the entry identifiers of its messaging user objects and a different **MAPIUID** to use for distribution lists.</span></span> 
    
<span data-ttu-id="5b78c-125">Quando houver vários objetos de logon que estão ativos simultaneamente, faz sentido ter estruturas **MAPIUID** exclusivas para cada um deles.</span><span class="sxs-lookup"><span data-stu-id="5b78c-125">When there are multiple logon objects that are concurrently active, it makes sense to have unique **MAPIUID** structures for each one.</span></span> <span data-ttu-id="5b78c-126">Isso aumenta a precisão com a qual o MAPI faz a correspondência de identificadores de entrada com provedores de serviços e salva algum trabalho.</span><span class="sxs-lookup"><span data-stu-id="5b78c-126">This increases the accuracy with which MAPI matches entry identifiers to service providers and saves some work.</span></span> <span data-ttu-id="5b78c-127">Quando cada objeto de logon tem seu próprio identificador exclusivo, MAPI pode garantir que qualquer solicitação rotas a um objeto de logon podem ser administradas por esse objeto.</span><span class="sxs-lookup"><span data-stu-id="5b78c-127">When every logon object has its own unique identifier, MAPI can guarantee that any request it routes to a logon object can be handled by that object.</span></span> <span data-ttu-id="5b78c-128">Quando os objetos de logon compartilham **MAPIUID** estruturas, MAPI encaminha a solicitação para o primeiro objeto de logon que é identificado pelo **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="5b78c-128">When logon objects share **MAPIUID** structures, MAPI routes the request to the first logon object that is identified by the **MAPIUID**.</span></span> <span data-ttu-id="5b78c-129">Se um dos seus objetos logon recebe uma solicitação que não pode ser processada porque não processa o identificador de entrada, passa a solicitação de logon no seu próximo objeto logon antes de retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="5b78c-129">If one of your logon objects receives a request that it cannot process because it does not handle the entry identifier, pass the request on to your next logon object before returning an error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5b78c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b78c-130">See also</span></span>



[<span data-ttu-id="5b78c-131">Implementar o logon do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="5b78c-131">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

