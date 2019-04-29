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
# <a name="registering-service-provider-unique-identifiers"></a><span data-ttu-id="b8573-103">Registrando identificadores exclusivos do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="b8573-103">Registering Service Provider Unique Identifiers</span></span>

  
  
<span data-ttu-id="b8573-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8573-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8573-105">O catálogo de endereços, o repositório de mensagens e os provedores de transporte usam um identificador exclusivo conhecido como [MAPIUID](mapiuid.md) para registrar os objetos de serviço de vários tipos.</span><span class="sxs-lookup"><span data-stu-id="b8573-105">Address book, message store, and transport providers use a unique identifier known as a [MAPIUID](mapiuid.md) to register to service objects of various types.</span></span> <span data-ttu-id="b8573-106">Um **MAPIUID** é um identificador de 16 bytes que contém um GUID.</span><span class="sxs-lookup"><span data-stu-id="b8573-106">A **MAPIUID** is a 16-byte identifier that contains a GUID.</span></span> <span data-ttu-id="b8573-107">Você pode criar um **MAPIUID** usando o procedimento a seguir:</span><span class="sxs-lookup"><span data-stu-id="b8573-107">You can create a **MAPIUID** by using the following procedure:</span></span> 
  
1. <span data-ttu-id="b8573-108">Definir uma constante.</span><span class="sxs-lookup"><span data-stu-id="b8573-108">Define a constant.</span></span>
    
2. <span data-ttu-id="b8573-109">Invocar a ferramenta*Create GUID*\* do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b8573-109">Invoke the Visual Studio*Create GUID*\* tool.</span></span> 
    
<span data-ttu-id="b8573-110">Por exemplo, um provedor de catálogo de endereços pode incluir a constante a seguir em um arquivo de cabeçalho para definir um **MAPIUID**:</span><span class="sxs-lookup"><span data-stu-id="b8573-110">For example, an address book provider might include the following constant in a header file to define a **MAPIUID**:</span></span>
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 <span data-ttu-id="b8573-111">**Para registrar um MAPIUID se o seu provedor for um catálogo de endereços ou provedor de repositório de mensagens**</span><span class="sxs-lookup"><span data-stu-id="b8573-111">**To register a MAPIUID if your provider is an address book or message store provider**</span></span>
  
1. <span data-ttu-id="b8573-112">Chamar [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="b8573-112">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
    
2. <span data-ttu-id="b8573-113">Registre um **MAPIUID** para cada objeto de logon que você instancia e inclua esse **MAPIUID** nos primeiros 16 bytes do membro **AB** de cada identificador de entrada que você criar.</span><span class="sxs-lookup"><span data-stu-id="b8573-113">Register a **MAPIUID** for each logon object that you instantiate and include this **MAPIUID** in the first 16 bytes of the **ab** member of every entry identifier that you create.</span></span> <span data-ttu-id="b8573-114">MAPI usa estruturas **MAPIUID** para associar objetos com provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="b8573-114">MAPI uses **MAPIUID** structures to associate objects with service providers.</span></span> <span data-ttu-id="b8573-115">Quando um cliente chama o método [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir um objeto, o MAPI examina a parte **MAPIUID** do identificador de entrada, fazendo a correspondência com base no **MAPIUID**registrado, para determinar qual objeto de logon deve receber a abertura pedir.</span><span class="sxs-lookup"><span data-stu-id="b8573-115">When a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open an object, MAPI examines the **MAPIUID** portion of the entry identifier, matching it against the registered **MAPIUID**, to determine which logon object should receive the open request.</span></span>
    
3. <span data-ttu-id="b8573-116">Se seu provedor for um transporte, registre uma ou mais estruturas **MAPIUID** quando o MAPI chamar o método **IXPLogon:: AddressTypes** .</span><span class="sxs-lookup"><span data-stu-id="b8573-116">If your provider is a transport, register one or more **MAPIUID** structures when MAPI calls your **IXPLogon::AddressTypes** method.</span></span> <span data-ttu-id="b8573-117">MAPI usa as estruturas **MAPIUID** registradas por provedores de transporte para atribuir responsabilidade para entrega de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b8573-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span></span> 
    
<span data-ttu-id="b8573-118">Embora os provedores de serviços normalmente registrem um único **MAPIUID**, você pode registrar várias estruturas do **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="b8573-118">Although service providers typically register a single **MAPIUID**, you can register multiple **MAPIUID** structures.</span></span> <span data-ttu-id="b8573-119">Se o seu catálogo de endereços ou provedor de mensagens suportar vários objetos de logon, talvez por permitir que um usuário adicione mais de uma instância do seu provedor ao seu perfil, talvez você queira implementar um **MAPIUID** diferente para cada objeto de logon.</span><span class="sxs-lookup"><span data-stu-id="b8573-119">If your address book or message store provider supports multiple logon objects, perhaps by permitting a user to add more than one instance of your provider to their profile, you might want to implement a different **MAPIUID** for each logon object.</span></span> <span data-ttu-id="b8573-120">Há alguns outros motivos para suportar mais de um **MAPIUID**:</span><span class="sxs-lookup"><span data-stu-id="b8573-120">There are a few other reasons to support more than one **MAPIUID**:</span></span>
  
- <span data-ttu-id="b8573-121">Você deve dar suporte a mais de uma versão de seu provedor e os identificadores de entrada devem representar a versão apropriada.</span><span class="sxs-lookup"><span data-stu-id="b8573-121">You must support more than one version of your provider and the entry identifiers must represent the appropriate version.</span></span> <span data-ttu-id="b8573-122">Atribua um **MAPIUID** diferente para cada versão.</span><span class="sxs-lookup"><span data-stu-id="b8573-122">Assign a different **MAPIUID** for each version.</span></span> 
    
- <span data-ttu-id="b8573-123">Você deseja distinguir entre os tipos de objetos com suporte.</span><span class="sxs-lookup"><span data-stu-id="b8573-123">You want to distinguish between the types of objects you support.</span></span> <span data-ttu-id="b8573-124">Por exemplo, um provedor de catálogo de endereços pode querer registrar um **MAPIUID** para usar nos identificadores de entrada de seus objetos de usuário de mensagens e um **MAPIUID** diferente para usar para listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="b8573-124">For example, an address book provider might want to register one **MAPIUID** to use in the entry identifiers of its messaging user objects and a different **MAPIUID** to use for distribution lists.</span></span> 
    
<span data-ttu-id="b8573-125">Quando há vários objetos de logon simultaneamente ativos, faz sentido ter estruturas **MAPIUID** exclusivas para cada um.</span><span class="sxs-lookup"><span data-stu-id="b8573-125">When there are multiple logon objects that are concurrently active, it makes sense to have unique **MAPIUID** structures for each one.</span></span> <span data-ttu-id="b8573-126">Isso aumenta a precisão com a qual o MAPI corresponde a identificadores de entrada para os provedores de serviço e salva algum trabalho.</span><span class="sxs-lookup"><span data-stu-id="b8573-126">This increases the accuracy with which MAPI matches entry identifiers to service providers and saves some work.</span></span> <span data-ttu-id="b8573-127">Quando cada objeto de logon tem seu próprio identificador exclusivo, o MAPI pode garantir que qualquer solicitação que ele roteia para um objeto de logon possa ser tratada por esse objeto.</span><span class="sxs-lookup"><span data-stu-id="b8573-127">When every logon object has its own unique identifier, MAPI can guarantee that any request it routes to a logon object can be handled by that object.</span></span> <span data-ttu-id="b8573-128">Quando os objetos de logon compartilham estruturas do **MAPIUID** , o MAPI encaminha a solicitação para o primeiro objeto de logon identificado pelo **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="b8573-128">When logon objects share **MAPIUID** structures, MAPI routes the request to the first logon object that is identified by the **MAPIUID**.</span></span> <span data-ttu-id="b8573-129">Se um dos seus objetos de logon receber uma solicitação que ele não pode processar porque ele não lida com o identificador de entrada, passe a solicitação para o seu próximo objeto de logon antes de retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="b8573-129">If one of your logon objects receives a request that it cannot process because it does not handle the entry identifier, pass the request on to your next logon object before returning an error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b8573-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8573-130">See also</span></span>



[<span data-ttu-id="b8573-131">Implementar o logon do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="b8573-131">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

