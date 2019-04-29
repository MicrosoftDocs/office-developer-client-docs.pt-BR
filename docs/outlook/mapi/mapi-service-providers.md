---
title: Provedores de serviço MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bb40891376ac511869ba157b675e53ee236b24ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409535"
---
# <a name="mapi-service-providers"></a><span data-ttu-id="75f57-103">Provedores de serviço MAPI</span><span class="sxs-lookup"><span data-stu-id="75f57-103">MAPI Service Providers</span></span>

  
  
<span data-ttu-id="75f57-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75f57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75f57-105">Há três tipos comuns de provedores de serviços:</span><span class="sxs-lookup"><span data-stu-id="75f57-105">There are three common types of service providers:</span></span>
  
- <span data-ttu-id="75f57-106">Provedores de catálogos de endereços.</span><span class="sxs-lookup"><span data-stu-id="75f57-106">Address book providers.</span></span>
    
- <span data-ttu-id="75f57-107">Provedores do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="75f57-107">Message store providers.</span></span>
    
- <span data-ttu-id="75f57-108">Provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="75f57-108">Transport providers.</span></span>
    
<span data-ttu-id="75f57-109">Os provedores de catálogo de endereços e de repositório de mensagens têm muitas semelhanças.</span><span class="sxs-lookup"><span data-stu-id="75f57-109">Address book and message store providers have many similarities.</span></span> <span data-ttu-id="75f57-110">Eles registram um identificador exclusivo com MAPI que eles usam para construir identificadores de entrada para seus objetos.</span><span class="sxs-lookup"><span data-stu-id="75f57-110">They register a unique identifier with MAPI that they use for constructing entry identifiers for their objects.</span></span> <span data-ttu-id="75f57-111">Eles fornecem uma hierarquia de objetos e propriedades que os clientes podem acessar e manipular.</span><span class="sxs-lookup"><span data-stu-id="75f57-111">They provide a hierarchy of objects and properties that clients can access and manipulate.</span></span> <span data-ttu-id="75f57-112">Para seus objetos contêiner, eles dão suporte a uma tabela de hierarquia e a uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="75f57-112">For their container objects, they support a hierarchy table and a contents table.</span></span> <span data-ttu-id="75f57-113">Eles dão suporte à notificação de eventos nessas tabelas e, opcionalmente, em objetos individuais para que os clientes possam ser informados sobre alterações que ocorrem durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="75f57-113">They support event notification on these tables and optionally on individual objects so that clients can be informed of changes that occur during the session.</span></span> <span data-ttu-id="75f57-114">Quando as operações se tornam longas, elas podem exibir um indicador de progresso para informar o usuário sobre o status da operação.</span><span class="sxs-lookup"><span data-stu-id="75f57-114">When operations become lengthy, they can display a progress indicator to inform the user of the operation's status.</span></span> <span data-ttu-id="75f57-115">Os clientes podem se comunicar com o catálogo de endereços e os provedores de repositórios de mensagens indiretamente por meio de MAPI usando as interfaces [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) e [IMAPISession: IUnknown](imapisessioniunknown.md) ou diretamente usando uma das interfaces de provedor de serviços no tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="75f57-115">Clients can communicate with address book and message store providers either indirectly through MAPI by using the [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) and [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces or directly by using one of the service provider interfaces in the following table.</span></span> 
  
|<span data-ttu-id="75f57-116">**Interfaces do provedor de catálogo de endereços**</span><span class="sxs-lookup"><span data-stu-id="75f57-116">**Address book provider interfaces**</span></span>|<span data-ttu-id="75f57-117">**Interfaces do provedor de repositório de mensagens**</span><span class="sxs-lookup"><span data-stu-id="75f57-117">**Message store provider interfaces**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75f57-118">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="75f57-118">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md) <br/> |[<span data-ttu-id="75f57-119">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="75f57-119">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md) <br/> |
|[<span data-ttu-id="75f57-120">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="75f57-120">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md) <br/> |[<span data-ttu-id="75f57-121">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="75f57-121">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md) <br/> |
|[<span data-ttu-id="75f57-122">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="75f57-122">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md) <br/> |[<span data-ttu-id="75f57-123">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="75f57-123">IMessage : IMAPIProp</span></span>](imessageimapiprop.md) <br/> |
| <br/> |[<span data-ttu-id="75f57-124">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="75f57-124">IAttach : IMAPIProp</span></span>](iattachimapiprop.md) <br/> |
   
<span data-ttu-id="75f57-125">Os provedores de transporte diferem dos provedores de catálogo de endereços e de repositório de mensagens no modo como se comunicam com MAPI e com clientes.</span><span class="sxs-lookup"><span data-stu-id="75f57-125">Transport providers differ from address book and message store providers in the way they communicate with MAPI and with clients.</span></span> <span data-ttu-id="75f57-126">Geralmente, os provedores de transporte esperam por MAPI solicitar informações em vez de iniciar a comunicação.</span><span class="sxs-lookup"><span data-stu-id="75f57-126">Transport providers typically wait for MAPI to prompt them for information rather than initiate communication.</span></span> <span data-ttu-id="75f57-127">Diferentemente dos outros provedores, os provedores de transporte não dão suporte a uma variedade de objetos e tabelas que são comumente acessados por clientes.</span><span class="sxs-lookup"><span data-stu-id="75f57-127">Unlike the other providers, transport providers do not support a variety of objects and tables that are commonly accessed by clients.</span></span> <span data-ttu-id="75f57-128">No enTanto, eles dão suporte a um objeto status, como todos os provedores de serviço e publica suas propriedades na tabela de status.</span><span class="sxs-lookup"><span data-stu-id="75f57-128">However, they do support a status object, as do all service providers, and publish its properties in the status table.</span></span> <span data-ttu-id="75f57-129">Enquanto o catálogo de endereços e os provedores de repositório de mensagens chamam o método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) para registrar identificadores exclusivos para construir seus identificadores de entrada, os provedores de transporte chamam o método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) para Registre os identificadores exclusivos, bem como os tipos de endereço para assumir a responsabilidade da entrega de mensagens específicas.</span><span class="sxs-lookup"><span data-stu-id="75f57-129">Whereas address book and message store providers call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register unique identifiers for constructing their entry identifiers, transport providers call the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to register unique identifiers, as well as address types for assuming responsibility for the delivery of particular messages.</span></span> 
  
<span data-ttu-id="75f57-130">Seu provedor de serviços deve ter três arquivos de cabeçalho: um arquivo de cabeçalho público e dois arquivos internos.</span><span class="sxs-lookup"><span data-stu-id="75f57-130">Your service provider should have three header files: one public header file and two internal files.</span></span> <span data-ttu-id="75f57-131">Use o arquivo de cabeçalho público para configuração e para documentar Propriedades e seus valores.</span><span class="sxs-lookup"><span data-stu-id="75f57-131">Use the public header file for configuration and for documenting properties and their values.</span></span> <span data-ttu-id="75f57-132">Inclua um dos arquivos de cabeçalho internos todos os cabeçalhos MAPI públicos necessários; Esse arquivo de cabeçalho deve ser incluído em todos os arquivos de origem do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="75f57-132">Include in one of the internal header files all the necessary public MAPI headers; this header file should be included in all of your service provider source files.</span></span> <span data-ttu-id="75f57-133">Use o outro arquivo interno para definir identificadores de recurso.</span><span class="sxs-lookup"><span data-stu-id="75f57-133">Use the other internal file to define resource identifiers.</span></span>
  
<span data-ttu-id="75f57-134">Catálogo de endereços, repositório de mensagens e provedores de transporte execute as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="75f57-134">Address book, message store, and transport providers perform the following tasks:</span></span>
  
- <span data-ttu-id="75f57-135">Forneça uma função de ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="75f57-135">Supply an entry point function.</span></span> 
    
- <span data-ttu-id="75f57-136">Forneça um provedor e um objeto de logon para manipular o logon e a inicialização.</span><span class="sxs-lookup"><span data-stu-id="75f57-136">Supply a provider and logon object to handle logon and initialization.</span></span> 
    
- <span data-ttu-id="75f57-137">Se o provedor pertencer a um serviço de mensagens, forneça uma função de ponto de entrada do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="75f57-137">If the provider belongs to a message service, supply a message service entry point function.</span></span> 
    
- <span data-ttu-id="75f57-138">Suporte à configuração implementando uma folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="75f57-138">Support configuration by implementing a property sheet.</span></span>
    
- <span data-ttu-id="75f57-139">Implemente um objeto status e dê suporte à tabela status.</span><span class="sxs-lookup"><span data-stu-id="75f57-139">Implement a status object and support the status table.</span></span> 
    
- <span data-ttu-id="75f57-140">Controle de desligamento.</span><span class="sxs-lookup"><span data-stu-id="75f57-140">Handle shut down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75f57-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="75f57-141">See also</span></span>



[<span data-ttu-id="75f57-142">Conceitos de MAPI</span><span class="sxs-lookup"><span data-stu-id="75f57-142">MAPI Concepts</span></span>](mapi-concepts.md)

