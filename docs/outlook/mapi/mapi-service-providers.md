---
title: Provedores de serviços MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1f931382e790da13e7d4a746e286d9dc176b7b6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571903"
---
# <a name="mapi-service-providers"></a><span data-ttu-id="550c4-103">Provedores de serviços MAPI</span><span class="sxs-lookup"><span data-stu-id="550c4-103">MAPI Service Providers</span></span>

  
  
<span data-ttu-id="550c4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="550c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="550c4-105">Existem três tipos comuns de provedores de serviços:</span><span class="sxs-lookup"><span data-stu-id="550c4-105">There are three common types of service providers:</span></span>
  
- <span data-ttu-id="550c4-106">Provedores de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="550c4-106">Address book providers.</span></span>
    
- <span data-ttu-id="550c4-107">Provedores de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="550c4-107">Message store providers.</span></span>
    
- <span data-ttu-id="550c4-108">Provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="550c4-108">Transport providers.</span></span>
    
<span data-ttu-id="550c4-109">Provedores de armazenamento de mensagens e catálogo de endereço têm muitas semelhanças.</span><span class="sxs-lookup"><span data-stu-id="550c4-109">Address book and message store providers have many similarities.</span></span> <span data-ttu-id="550c4-110">Eles registram um identificador exclusivo com MAPI empregados para construir identificadores de entrada para seus objetos.</span><span class="sxs-lookup"><span data-stu-id="550c4-110">They register a unique identifier with MAPI that they use for constructing entry identifiers for their objects.</span></span> <span data-ttu-id="550c4-111">Eles fornecem uma hierarquia de objetos e propriedades que os clientes podem acessar e manipular.</span><span class="sxs-lookup"><span data-stu-id="550c4-111">They provide a hierarchy of objects and properties that clients can access and manipulate.</span></span> <span data-ttu-id="550c4-112">Para seus objetos de contêiner, eles suportam uma tabela de hierarquia e uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="550c4-112">For their container objects, they support a hierarchy table and a contents table.</span></span> <span data-ttu-id="550c4-113">Eles suportam notificação de evento nestas tabelas e, opcionalmente, em objetos individuais para que os clientes podem ser informados sobre alterações que ocorrem durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="550c4-113">They support event notification on these tables and optionally on individual objects so that clients can be informed of changes that occur during the session.</span></span> <span data-ttu-id="550c4-114">Quando operações ficam longas, eles podem exibir um indicador de progresso para informar ao usuário sobre o status da operação.</span><span class="sxs-lookup"><span data-stu-id="550c4-114">When operations become lengthy, they can display a progress indicator to inform the user of the operation's status.</span></span> <span data-ttu-id="550c4-115">Os clientes podem se comunicar com provedores de armazenamento de mensagens e catálogo de endereço qualquer MAPI indiretamente até usando o [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) e [IMAPISession: IUnknown](imapisessioniunknown.md) interfaces ou diretamente usando com uma das interfaces do provedor de serviço no tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="550c4-115">Clients can communicate with address book and message store providers either indirectly through MAPI by using the [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) and [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces or directly by using one of the service provider interfaces in the following table.</span></span> 
  
|<span data-ttu-id="550c4-116">**Interfaces do provedor de catálogo de endereços**</span><span class="sxs-lookup"><span data-stu-id="550c4-116">**Address book provider interfaces**</span></span>|<span data-ttu-id="550c4-117">**Interfaces do provedor de repositório de mensagem**</span><span class="sxs-lookup"><span data-stu-id="550c4-117">**Message store provider interfaces**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="550c4-118">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="550c4-118">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md) <br/> |[<span data-ttu-id="550c4-119">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="550c4-119">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md) <br/> |
|[<span data-ttu-id="550c4-120">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="550c4-120">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md) <br/> |[<span data-ttu-id="550c4-121">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="550c4-121">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md) <br/> |
|[<span data-ttu-id="550c4-122">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="550c4-122">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md) <br/> |[<span data-ttu-id="550c4-123">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="550c4-123">IMessage : IMAPIProp</span></span>](imessageimapiprop.md) <br/> |
| <br/> |[<span data-ttu-id="550c4-124">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="550c4-124">IAttach : IMAPIProp</span></span>](iattachimapiprop.md) <br/> |
   
<span data-ttu-id="550c4-125">Provedores de transporte diferem dos provedores de armazenamento mensagens e catálogo de endereço da maneira que se comunicam com MAPI e com clientes.</span><span class="sxs-lookup"><span data-stu-id="550c4-125">Transport providers differ from address book and message store providers in the way they communicate with MAPI and with clients.</span></span> <span data-ttu-id="550c4-126">Provedores de transporte normalmente Aguarde MAPI-los solicitar informações ao invés de iniciar a comunicação.</span><span class="sxs-lookup"><span data-stu-id="550c4-126">Transport providers typically wait for MAPI to prompt them for information rather than initiate communication.</span></span> <span data-ttu-id="550c4-127">Ao contrário de outros provedores, provedores de transporte não suportam uma variedade de objetos e tabelas que costumam ser acessadas pelos clientes.</span><span class="sxs-lookup"><span data-stu-id="550c4-127">Unlike the other providers, transport providers do not support a variety of objects and tables that are commonly accessed by clients.</span></span> <span data-ttu-id="550c4-128">No entanto, eles têm suporte para um objeto de status, conforme faça todos os provedores de serviço e publicar suas propriedades da tabela de status.</span><span class="sxs-lookup"><span data-stu-id="550c4-128">However, they do support a status object, as do all service providers, and publish its properties in the status table.</span></span> <span data-ttu-id="550c4-129">Enquanto os provedores de armazenamento de mensagens e catálogo de endereço chamarem o método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar os identificadores exclusivos para construir seus identificadores de entrada, chamarem o método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para ThisDocument provedores de transporte Registre os identificadores exclusivos, bem como tipos de endereço de assumindo a responsabilidade para a entrega de mensagens específicas.</span><span class="sxs-lookup"><span data-stu-id="550c4-129">Whereas address book and message store providers call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register unique identifiers for constructing their entry identifiers, transport providers call the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to register unique identifiers, as well as address types for assuming responsibility for the delivery of particular messages.</span></span> 
  
<span data-ttu-id="550c4-130">Seu provedor de serviços deve ter os três arquivos de cabeçalho: um arquivo de cabeçalho público e dois arquivos internos.</span><span class="sxs-lookup"><span data-stu-id="550c4-130">Your service provider should have three header files: one public header file and two internal files.</span></span> <span data-ttu-id="550c4-131">Use o arquivo de cabeçalho público para a configuração e para documentar as propriedades e seus valores.</span><span class="sxs-lookup"><span data-stu-id="550c4-131">Use the public header file for configuration and for documenting properties and their values.</span></span> <span data-ttu-id="550c4-132">Incluir em um dos arquivos de cabeçalho interno todos os necessário pública MAPI cabeçalhos; Este arquivo de cabeçalho deve ser incluído em todos os seus arquivos de origem de provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="550c4-132">Include in one of the internal header files all the necessary public MAPI headers; this header file should be included in all of your service provider source files.</span></span> <span data-ttu-id="550c4-133">Use o outro arquivo interno para definir os identificadores de recurso.</span><span class="sxs-lookup"><span data-stu-id="550c4-133">Use the other internal file to define resource identifiers.</span></span>
  
<span data-ttu-id="550c4-134">Catálogo de endereços, armazenamento de mensagens e provedores de transporte executam as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="550c4-134">Address book, message store, and transport providers perform the following tasks:</span></span>
  
- <span data-ttu-id="550c4-135">Fornece uma função de ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="550c4-135">Supply an entry point function.</span></span> 
    
- <span data-ttu-id="550c4-136">Fornece um provedor e o objeto de logon para lidar com o logon e inicialização.</span><span class="sxs-lookup"><span data-stu-id="550c4-136">Supply a provider and logon object to handle logon and initialization.</span></span> 
    
- <span data-ttu-id="550c4-137">Se o provedor pertence a um serviço de mensagem, fornece uma função de ponto de entrada de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="550c4-137">If the provider belongs to a message service, supply a message service entry point function.</span></span> 
    
- <span data-ttu-id="550c4-138">Suporte a configuração por meio da implementação de uma folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="550c4-138">Support configuration by implementing a property sheet.</span></span>
    
- <span data-ttu-id="550c4-139">Um objeto de status de implementar e oferecer suporte a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="550c4-139">Implement a status object and support the status table.</span></span> 
    
- <span data-ttu-id="550c4-140">Alça desligado.</span><span class="sxs-lookup"><span data-stu-id="550c4-140">Handle shut down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="550c4-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="550c4-141">See also</span></span>



[<span data-ttu-id="550c4-142">Conceitos MAPI</span><span class="sxs-lookup"><span data-stu-id="550c4-142">MAPI Concepts</span></span>](mapi-concepts.md)

