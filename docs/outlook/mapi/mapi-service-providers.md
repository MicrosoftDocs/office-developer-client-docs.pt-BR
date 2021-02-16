---
title: Provedores de Serviços MAPI
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
# <a name="mapi-service-providers"></a><span data-ttu-id="8b961-103">Provedores de Serviços MAPI</span><span class="sxs-lookup"><span data-stu-id="8b961-103">MAPI Service Providers</span></span>

  
  
<span data-ttu-id="8b961-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b961-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b961-105">Existem três tipos comuns de provedores de serviços:</span><span class="sxs-lookup"><span data-stu-id="8b961-105">There are three common types of service providers:</span></span>
  
- <span data-ttu-id="8b961-106">Provedores de lista de endereços.</span><span class="sxs-lookup"><span data-stu-id="8b961-106">Address book providers.</span></span>
    
- <span data-ttu-id="8b961-107">Provedores de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="8b961-107">Message store providers.</span></span>
    
- <span data-ttu-id="8b961-108">Provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="8b961-108">Transport providers.</span></span>
    
<span data-ttu-id="8b961-109">Os provedores de armazenamento de mensagens e de address book têm muitas semelhanças.</span><span class="sxs-lookup"><span data-stu-id="8b961-109">Address book and message store providers have many similarities.</span></span> <span data-ttu-id="8b961-110">Eles registram um identificador exclusivo com MAPI que usam para construir identificadores de entrada para seus objetos.</span><span class="sxs-lookup"><span data-stu-id="8b961-110">They register a unique identifier with MAPI that they use for constructing entry identifiers for their objects.</span></span> <span data-ttu-id="8b961-111">Eles fornecem uma hierarquia de objetos e propriedades que os clientes podem acessar e manipular.</span><span class="sxs-lookup"><span data-stu-id="8b961-111">They provide a hierarchy of objects and properties that clients can access and manipulate.</span></span> <span data-ttu-id="8b961-112">Para seus objetos contêineres, eles suportam uma tabela de hierarquia e uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="8b961-112">For their container objects, they support a hierarchy table and a contents table.</span></span> <span data-ttu-id="8b961-113">Eles suportam a notificação de evento nessas tabelas e, opcionalmente, em objetos individuais, para que os clientes possam ser informados das alterações que ocorrem durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="8b961-113">They support event notification on these tables and optionally on individual objects so that clients can be informed of changes that occur during the session.</span></span> <span data-ttu-id="8b961-114">Quando as operações se tornam demoradas, elas podem exibir um indicador de progresso para informar o usuário sobre o status da operação.</span><span class="sxs-lookup"><span data-stu-id="8b961-114">When operations become lengthy, they can display a progress indicator to inform the user of the operation's status.</span></span> <span data-ttu-id="8b961-115">Os clientes podem se comunicar com o livro de endereços e provedores de armazenamento de mensagens indiretamente através de MAPI usando [o IAddrBook : IMAPIProp](iaddrbookimapiprop.md) e [IMAPISession : interfaces IUnknown](imapisessioniunknown.md) ou diretamente usando uma das interfaces do provedor de serviços na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b961-115">Clients can communicate with address book and message store providers either indirectly through MAPI by using the [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) and [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces or directly by using one of the service provider interfaces in the following table.</span></span> 
  
|<span data-ttu-id="8b961-116">**Interfaces do provedor de agendas**</span><span class="sxs-lookup"><span data-stu-id="8b961-116">**Address book provider interfaces**</span></span>|<span data-ttu-id="8b961-117">**Interfaces do provedor do armazenamento de mensagens**</span><span class="sxs-lookup"><span data-stu-id="8b961-117">**Message store provider interfaces**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8b961-118">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="8b961-118">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md) <br/> |[<span data-ttu-id="8b961-119">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8b961-119">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md) <br/> |
|[<span data-ttu-id="8b961-120">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="8b961-120">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md) <br/> |[<span data-ttu-id="8b961-121">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="8b961-121">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md) <br/> |
|[<span data-ttu-id="8b961-122">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8b961-122">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md) <br/> |[<span data-ttu-id="8b961-123">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8b961-123">IMessage : IMAPIProp</span></span>](imessageimapiprop.md) <br/> |
| <br/> |[<span data-ttu-id="8b961-124">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8b961-124">IAttach : IMAPIProp</span></span>](iattachimapiprop.md) <br/> |
   
<span data-ttu-id="8b961-125">Os provedores de transporte diferem do livro de endereços e dos provedores de armazenamento de mensagens na maneira como se comunicam com MAPI e com clientes.</span><span class="sxs-lookup"><span data-stu-id="8b961-125">Transport providers differ from address book and message store providers in the way they communicate with MAPI and with clients.</span></span> <span data-ttu-id="8b961-126">Os provedores de transporte normalmente aguardam o MAPI solicitar informações em vez de iniciar a comunicação.</span><span class="sxs-lookup"><span data-stu-id="8b961-126">Transport providers typically wait for MAPI to prompt them for information rather than initiate communication.</span></span> <span data-ttu-id="8b961-127">Ao contrário dos outros provedores, os provedores de transporte não suportam uma variedade de objetos e tabelas que são comumente acessados por clientes.</span><span class="sxs-lookup"><span data-stu-id="8b961-127">Unlike the other providers, transport providers do not support a variety of objects and tables that are commonly accessed by clients.</span></span> <span data-ttu-id="8b961-128">No entanto, eles suportam um objeto de status, assim como todos os provedores de serviços, e publicam suas propriedades na tabela de status.</span><span class="sxs-lookup"><span data-stu-id="8b961-128">However, they do support a status object, as do all service providers, and publish its properties in the status table.</span></span> <span data-ttu-id="8b961-129">Enquanto os provedores de armazenamento de mensagens e de agendamento de endereços chamam o método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar identificadores exclusivos para construir seus identificadores de entrada, os provedores de transporte chamam o método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para registrar identificadores exclusivos, bem como os tipos de endereço para assumir a responsabilidade pela entrega de mensagens específicas.</span><span class="sxs-lookup"><span data-stu-id="8b961-129">Whereas address book and message store providers call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register unique identifiers for constructing their entry identifiers, transport providers call the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to register unique identifiers, as well as address types for assuming responsibility for the delivery of particular messages.</span></span> 
  
<span data-ttu-id="8b961-130">Seu provedor de serviços deve ter três arquivos de header: um arquivo de header público e dois arquivos internos.</span><span class="sxs-lookup"><span data-stu-id="8b961-130">Your service provider should have three header files: one public header file and two internal files.</span></span> <span data-ttu-id="8b961-131">Use o arquivo de header público para configuração e para documentar propriedades e seus valores.</span><span class="sxs-lookup"><span data-stu-id="8b961-131">Use the public header file for configuration and for documenting properties and their values.</span></span> <span data-ttu-id="8b961-132">Inclua em um dos arquivos de header internos todos os headers DE MAPI públicos necessários; esse arquivo de header deve ser incluído em todos os arquivos de origem do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="8b961-132">Include in one of the internal header files all the necessary public MAPI headers; this header file should be included in all of your service provider source files.</span></span> <span data-ttu-id="8b961-133">Use o outro arquivo interno para definir identificadores de recurso.</span><span class="sxs-lookup"><span data-stu-id="8b961-133">Use the other internal file to define resource identifiers.</span></span>
  
<span data-ttu-id="8b961-134">Os provedores de agenda, armazenamento de mensagens e transporte executam as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="8b961-134">Address book, message store, and transport providers perform the following tasks:</span></span>
  
- <span data-ttu-id="8b961-135">Fornecer uma função de ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="8b961-135">Supply an entry point function.</span></span> 
    
- <span data-ttu-id="8b961-136">Fornecer um provedor e um objeto de logon para lidar com o logon e a inicialização.</span><span class="sxs-lookup"><span data-stu-id="8b961-136">Supply a provider and logon object to handle logon and initialization.</span></span> 
    
- <span data-ttu-id="8b961-137">Se o provedor pertencer a um serviço de mensagens, fornecerá uma função de ponto de entrada do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="8b961-137">If the provider belongs to a message service, supply a message service entry point function.</span></span> 
    
- <span data-ttu-id="8b961-138">Suporte à configuração implementando uma folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8b961-138">Support configuration by implementing a property sheet.</span></span>
    
- <span data-ttu-id="8b961-139">Implemente um objeto de status e suporte a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="8b961-139">Implement a status object and support the status table.</span></span> 
    
- <span data-ttu-id="8b961-140">Tratar o desligar.</span><span class="sxs-lookup"><span data-stu-id="8b961-140">Handle shut down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b961-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b961-141">See also</span></span>



[<span data-ttu-id="8b961-142">Conceitos de MAPI</span><span class="sxs-lookup"><span data-stu-id="8b961-142">MAPI Concepts</span></span>](mapi-concepts.md)

