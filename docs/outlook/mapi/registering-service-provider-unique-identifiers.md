---
title: Registrando identificadores exclusivos do provedor de serviços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9f4acbb06f85a88a6c057da263ae95e09f72e0bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410172"
---
# <a name="registering-service-provider-unique-identifiers"></a><span data-ttu-id="e8892-103">Registrando identificadores exclusivos do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="e8892-103">Registering Service Provider Unique Identifiers</span></span>

  
  
<span data-ttu-id="e8892-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8892-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8892-105">Os provedores de transporte, armazenamento de mensagens e de agendamento de endereço usam um identificador exclusivo conhecido como [MAPIUID](mapiuid.md) para se registrar em objetos de serviço de vários tipos.</span><span class="sxs-lookup"><span data-stu-id="e8892-105">Address book, message store, and transport providers use a unique identifier known as a [MAPIUID](mapiuid.md) to register to service objects of various types.</span></span> <span data-ttu-id="e8892-106">Um **MAPIUID** é um identificador de 16 byte que contém um GUID.</span><span class="sxs-lookup"><span data-stu-id="e8892-106">A **MAPIUID** is a 16-byte identifier that contains a GUID.</span></span> <span data-ttu-id="e8892-107">Você pode criar um **MAPIUID** usando o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="e8892-107">You can create a **MAPIUID** by using the following procedure:</span></span> 
  
1. <span data-ttu-id="e8892-108">Defina uma constante.</span><span class="sxs-lookup"><span data-stu-id="e8892-108">Define a constant.</span></span>
    
2. <span data-ttu-id="e8892-109">Invoque a ferramenta *Criar GUID*\* do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e8892-109">Invoke the Visual Studio *Create GUID*\* tool.</span></span> 
    
<span data-ttu-id="e8892-110">Por exemplo, um provedor de livros de endereços pode incluir a seguinte constante em um arquivo de título para definir um **MAPIUID**:</span><span class="sxs-lookup"><span data-stu-id="e8892-110">For example, an address book provider might include the following constant in a header file to define a **MAPIUID**:</span></span>
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 <span data-ttu-id="e8892-111">**Para registrar um MAPIUID se seu provedor for um provedor de armazenamento de mensagens ou de um livro de endereços**</span><span class="sxs-lookup"><span data-stu-id="e8892-111">**To register a MAPIUID if your provider is an address book or message store provider**</span></span>
  
1. <span data-ttu-id="e8892-112">Chame [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="e8892-112">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
    
2. <span data-ttu-id="e8892-113">Registre **um MAPIUID** para cada objeto de logon que você criar e inclua esse **MAPIUID** nos primeiros 16 bytes do membro **ab** de cada identificador de entrada que você criar.</span><span class="sxs-lookup"><span data-stu-id="e8892-113">Register a **MAPIUID** for each logon object that you instantiate and include this **MAPIUID** in the first 16 bytes of the **ab** member of every entry identifier that you create.</span></span> <span data-ttu-id="e8892-114">O MAPI usa **estruturas MAPIUID** para associar objetos a provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="e8892-114">MAPI uses **MAPIUID** structures to associate objects with service providers.</span></span> <span data-ttu-id="e8892-115">Quando um cliente chama o método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir um objeto, o MAPI examina a parte **MAPIUID** do identificador de entrada, correspondendo-o ao **MAPIUID** registrado, para determinar qual objeto de logon deve receber a solicitação de abertura.</span><span class="sxs-lookup"><span data-stu-id="e8892-115">When a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open an object, MAPI examines the **MAPIUID** portion of the entry identifier, matching it against the registered **MAPIUID**, to determine which logon object should receive the open request.</span></span>
    
3. <span data-ttu-id="e8892-116">Se o provedor for um transporte, registre uma ou mais estruturas **MAPIUID** quando o MAPI chamar seu método **IXPLogon::AddressTypes.**</span><span class="sxs-lookup"><span data-stu-id="e8892-116">If your provider is a transport, register one or more **MAPIUID** structures when MAPI calls your **IXPLogon::AddressTypes** method.</span></span> <span data-ttu-id="e8892-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span><span class="sxs-lookup"><span data-stu-id="e8892-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span></span> 
    
<span data-ttu-id="e8892-118">Embora os provedores de serviços normalmente registrem um único **MAPIUID,** você pode registrar várias **estruturas MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="e8892-118">Although service providers typically register a single **MAPIUID**, you can register multiple **MAPIUID** structures.</span></span> <span data-ttu-id="e8892-119">Se o seu agendador de endereços ou o provedor de armazenamento de mensagens oferece suporte a vários objetos de logon, talvez permitindo que um usuário adicione mais de uma instância do seu provedor ao seu perfil, talvez você queira implementar um **MAPIUID** diferente para cada objeto de logon.</span><span class="sxs-lookup"><span data-stu-id="e8892-119">If your address book or message store provider supports multiple logon objects, perhaps by permitting a user to add more than one instance of your provider to their profile, you might want to implement a different **MAPIUID** for each logon object.</span></span> <span data-ttu-id="e8892-120">Há alguns outros motivos para dar suporte a mais de um **MAPIUID:**</span><span class="sxs-lookup"><span data-stu-id="e8892-120">There are a few other reasons to support more than one **MAPIUID**:</span></span>
  
- <span data-ttu-id="e8892-121">Você deve dar suporte a mais de uma versão do seu provedor, e os identificadores de entrada devem representar a versão apropriada.</span><span class="sxs-lookup"><span data-stu-id="e8892-121">You must support more than one version of your provider and the entry identifiers must represent the appropriate version.</span></span> <span data-ttu-id="e8892-122">Atribua um **MAPIUID diferente** para cada versão.</span><span class="sxs-lookup"><span data-stu-id="e8892-122">Assign a different **MAPIUID** for each version.</span></span> 
    
- <span data-ttu-id="e8892-123">Você deseja distinguir entre os tipos de objetos com suporte.</span><span class="sxs-lookup"><span data-stu-id="e8892-123">You want to distinguish between the types of objects you support.</span></span> <span data-ttu-id="e8892-124">Por exemplo, um provedor de agendamento de endereços pode querer registrar um **MAPIUID** a ser usado nos identificadores de entrada de seus objetos de usuário de mensagens e um **MAPIUID** diferente para usar em listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="e8892-124">For example, an address book provider might want to register one **MAPIUID** to use in the entry identifiers of its messaging user objects and a different **MAPIUID** to use for distribution lists.</span></span> 
    
<span data-ttu-id="e8892-125">Quando há vários objetos de logon atualmente ativos, faz sentido ter estruturas **MAPIUID** exclusivas para cada um deles.</span><span class="sxs-lookup"><span data-stu-id="e8892-125">When there are multiple logon objects that are concurrently active, it makes sense to have unique **MAPIUID** structures for each one.</span></span> <span data-ttu-id="e8892-126">Isso aumenta a precisão com a qual o MAPI corresponde aos identificadores de entrada para provedores de serviços e economiza algum trabalho.</span><span class="sxs-lookup"><span data-stu-id="e8892-126">This increases the accuracy with which MAPI matches entry identifiers to service providers and saves some work.</span></span> <span data-ttu-id="e8892-127">Quando cada objeto de logon tem seu próprio identificador exclusivo, o MAPI pode garantir que qualquer solicitação encaminhada a um objeto de logon possa ser manipulada por esse objeto.</span><span class="sxs-lookup"><span data-stu-id="e8892-127">When every logon object has its own unique identifier, MAPI can guarantee that any request it routes to a logon object can be handled by that object.</span></span> <span data-ttu-id="e8892-128">Quando objetos de logon compartilham estruturas **MAPIUID,** MAPI encaminha a solicitação para o primeiro objeto de logon identificado pela **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="e8892-128">When logon objects share **MAPIUID** structures, MAPI routes the request to the first logon object that is identified by the **MAPIUID**.</span></span> <span data-ttu-id="e8892-129">Se um dos objetos de logon receber uma solicitação que não pode processar porque não trata o identificador de entrada, passe a solicitação para o próximo objeto de logon antes de retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="e8892-129">If one of your logon objects receives a request that it cannot process because it does not handle the entry identifier, pass the request on to your next logon object before returning an error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e8892-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8892-130">See also</span></span>



[<span data-ttu-id="e8892-131">Implementando o logon do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="e8892-131">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

