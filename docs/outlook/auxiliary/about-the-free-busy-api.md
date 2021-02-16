---
title: Sobre a API do serviço de disponibilidade
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: A API de Livre/Ocupado permite que os provedores de email forneçam informações de status de livre/ocupado para contas de usuário especificadas dentro de um intervalo de tempo especificado.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433756"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="d0336-103">Sobre a API do serviço de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="d0336-103">About the Free/Busy API</span></span>

<span data-ttu-id="d0336-104">A API de Livre/Ocupado permite que os provedores de email forneçam informações de status de livre/ocupado para contas de usuário especificadas dentro de um intervalo de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="d0336-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="d0336-105">O status de livre/ocupado de um bloco de tempo no calendário de um usuário é um dos seguintes: fora do escritório, ocupado, provisório ou livre.</span><span class="sxs-lookup"><span data-stu-id="d0336-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="d0336-106">Criar um provedor de informações de livre/ocupado</span><span class="sxs-lookup"><span data-stu-id="d0336-106">Create a free/busy provider</span></span>

<span data-ttu-id="d0336-107">Para fornecer informações de livre/ocupado aos usuários de email, um provedor de email cria um provedor de informações de livre/ocupado e o registra no Outlook.</span><span class="sxs-lookup"><span data-stu-id="d0336-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="d0336-108">O provedor de informações de livre/ocupado deve implementar as interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="d0336-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="d0336-109">Observe que um número de membros nessas interfaces não é suportado e deve retornar os valores de retorno especificados.</span><span class="sxs-lookup"><span data-stu-id="d0336-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="d0336-110">Em particular, a API de Livre/Ocupado não dá suporte a acesso de gravação a informações de livre/ocupado e delegar acesso a contas.</span><span class="sxs-lookup"><span data-stu-id="d0336-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="d0336-111">[IFreeBusySupport](ifreebusysupport.md) — Essa interface dá suporte à especificação de interfaces que acessam dados de livre/ocupado para usuários especificados.</span><span class="sxs-lookup"><span data-stu-id="d0336-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="d0336-112">Ele usa [FBUser](fbuser.md) para identificar um usuário.</span><span class="sxs-lookup"><span data-stu-id="d0336-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="d0336-113">[IFreeBusyData](ifreebusydata.md) — essa interface obtém e define um intervalo de tempo para um determinado usuário e retorna uma interface para enumerar blocos de informações de livre/ocupado dentro desse intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="d0336-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="d0336-114">Ele usa o tempo relativo para obter e definir esse intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="d0336-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="d0336-115">Para obter mais informações, [consulte Usar o tempo relativo para acessar dados de livre/ocupado.](how-to-use-relative-time-to-access-free-busy-data.md)</span><span class="sxs-lookup"><span data-stu-id="d0336-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="d0336-116">[IEnumFBBlock](ienumfbblock.md) — Essa interface dá suporte ao acesso e à enumeração de blocos de informações de livre/ocupado para um usuário dentro de um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="d0336-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="d0336-117">Uma enumeração contém blocos de livre/ocupado que indicam o status de livre/ocupado dos períodos de tempo no calendário de um usuário, dentro de um intervalo de tempo (especificado por [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span><span class="sxs-lookup"><span data-stu-id="d0336-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="d0336-118">Itens em um calendário, como compromissos e solicitações de reunião, blocos de formulário na enumeração.</span><span class="sxs-lookup"><span data-stu-id="d0336-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="d0336-119">Os itens adjacentes entre si no calendário e que têm o mesmo status de livre/ocupado são combinados para formar um único bloco.</span><span class="sxs-lookup"><span data-stu-id="d0336-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="d0336-120">Um período de tempo livre em um calendário também forma um bloco.</span><span class="sxs-lookup"><span data-stu-id="d0336-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="d0336-121">Portanto, dois blocos consecutivos em uma enumeração não teriam o mesmo status de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="d0336-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="d0336-122">Esses blocos não se sobrepõem no tempo.</span><span class="sxs-lookup"><span data-stu-id="d0336-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="d0336-123">Quando há itens sobrepostos em um calendário, o Outlook mescla esses itens para formar blocos de disponibilidade não sobrepostos na enumeração com base nesta ordem de prioridade: ausência temporária, ocupado, provisório.</span><span class="sxs-lookup"><span data-stu-id="d0336-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="d0336-124">Para registrar o provedor de informações de livre/ocupado com o Outlook, o provedor de email deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d0336-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="d0336-125">Registre o provedor de informações de livre/ocupado com COM, fornecendo um CLSID que permite acesso à implementação do provedor **de IFreeBusySupport**.</span><span class="sxs-lookup"><span data-stu-id="d0336-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="d0336-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span><span class="sxs-lookup"><span data-stu-id="d0336-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="d0336-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span><span class="sxs-lookup"><span data-stu-id="d0336-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="d0336-128">Nome</span><span class="sxs-lookup"><span data-stu-id="d0336-128">Name</span></span> |<span data-ttu-id="d0336-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0336-129">Type</span></span> |<span data-ttu-id="d0336-130">Valor</span><span class="sxs-lookup"><span data-stu-id="d0336-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="d0336-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="d0336-131">SMTP</span></span>  |<span data-ttu-id="d0336-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="d0336-132">REG_SZ</span></span>  |<span data-ttu-id="d0336-133">{CLSID para a respectiva implementação de IFreeBusySupport}</span><span class="sxs-lookup"><span data-stu-id="d0336-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="d0336-134">Neste cenário, o Outlook cria a classe COM em coautoria e a usa para recuperar informações de livre/ocupado para qualquer usuário de email SMTP.</span><span class="sxs-lookup"><span data-stu-id="d0336-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="d0336-135">Para dar suporte a um agendador de endereços e provedor de transporte que use um tipo de entrada de endereço diferente de SMTP, altere  *o Nome* de acordo.</span><span class="sxs-lookup"><span data-stu-id="d0336-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d0336-136">Durante a instalação, os provedores de informações de livre/ocupado devem verificar se já existe uma configuração do Registro para o mesmo tipo de entrada de endereço.</span><span class="sxs-lookup"><span data-stu-id="d0336-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="d0336-137">Se isso acontecer, o provedor de informações de livre/ocupado deverá substituir o provedor atual por esse tipo de entrada de endereço e restaurá-lo quando ele for desinstalado.</span><span class="sxs-lookup"><span data-stu-id="d0336-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="d0336-138">No entanto, se um usuário tiver instalado mais de um provedor de informações para o mesmo tipo de entrada de endereço, o usuário deverá desinstalar esses provedores na ordem inversa da instalação (ou seja, sempre desinstalar o provedor mais recente).</span><span class="sxs-lookup"><span data-stu-id="d0336-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="d0336-139">Caso contrário, o Registro poderá apontar para um provedor que já tenha sido desinstalado.</span><span class="sxs-lookup"><span data-stu-id="d0336-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="d0336-140">Componentes da API</span><span class="sxs-lookup"><span data-stu-id="d0336-140">API components</span></span>

<span data-ttu-id="d0336-141">A API de Livre/Ocupado inclui os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="d0336-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="d0336-142">Definições</span><span class="sxs-lookup"><span data-stu-id="d0336-142">Definitions</span></span>

- [<span data-ttu-id="d0336-143">Constantes (API do serviço de disponibilidade)</span><span class="sxs-lookup"><span data-stu-id="d0336-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="d0336-144">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="d0336-144">Data types</span></span>

- [<span data-ttu-id="d0336-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="d0336-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="d0336-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="d0336-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="d0336-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="d0336-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="d0336-148">Interfaces</span><span class="sxs-lookup"><span data-stu-id="d0336-148">Interfaces</span></span>

- [<span data-ttu-id="d0336-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="d0336-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="d0336-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="d0336-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="d0336-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="d0336-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

