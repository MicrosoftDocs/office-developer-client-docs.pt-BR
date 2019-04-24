---
title: Sobre a API do serviço de disponibilidade
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: A API de disponibilidade permite que os provedores de email forneçam informações de status de disponibilidade para contas de usuário especificadas em um intervalo de tempo especificado.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317007"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="f0bcb-103">Sobre a API do serviço de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="f0bcb-103">About the Free/Busy API</span></span>

<span data-ttu-id="f0bcb-104">A API de disponibilidade permite que os provedores de email forneçam informações de status de disponibilidade para contas de usuário especificadas em um intervalo de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="f0bcb-105">O status de disponibilidade de um bloco de tempo no calendário de um usuário é um dos seguintes: fora do escritório, ocupado, provisório ou gratuito.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="f0bcb-106">Criar um provedor de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="f0bcb-106">Create a free/busy provider</span></span>

<span data-ttu-id="f0bcb-107">Para fornecer informações de disponibilidade para usuários de email, um provedor de email cria um provedor de disponibilidade e o registra com o Outlook.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="f0bcb-108">O provedor de disponibilidade deve implementar as seguintes interfaces.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="f0bcb-109">Observe que não há suporte para vários membros nessas interfaces e deve retornar os valores de retorno especificados.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="f0bcb-110">Em particular, a API de disponibilidade não suporta acesso de gravação para informações de disponibilidade e acesso de representante a contas.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="f0bcb-111">[IFreeBusySupport](ifreebusysupport.md) – esta interface suporta a especificação de interfaces que acessam dados de disponibilidade para usuários específicos.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="f0bcb-112">Ele usa [FBUser](fbuser.md) para identificar um usuário.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="f0bcb-113">[IFreeBusyData](ifreebusydata.md) – esta interface obtém e define um intervalo de tempo para um determinado usuário e retorna uma interface para enumerar blocos de disponibilidade de dados dentro desse intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="f0bcb-114">Ele usa o tempo relativo para obter e definir esse intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="f0bcb-115">Para obter mais informações, consulte [usar tempo relativo para acessar dados de disponibilidade](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="f0bcb-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="f0bcb-116">[IEnumFBBlock](ienumfbblock.md) — essa interface suporta o acesso e a enumeração de blocos de disponibilidade de dados para um usuário em um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="f0bcb-117">Uma enumeração contém blocos de disponibilidade que indicam o status de disponibilidade dos períodos de tempo no calendário de um usuário, dentro de um intervalo de tempo (especificado por [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md)).</span><span class="sxs-lookup"><span data-stu-id="f0bcb-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="f0bcb-118">Itens em um calendário, como compromissos e solicitações de reunião, blocos de formulários na enumeração.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="f0bcb-119">Os itens que estão adjacentes entre si no calendário e têm o mesmo status de disponibilidade são combinados para formar um único bloco.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="f0bcb-120">Um período de tempo gratuito em um calendário também forma um bloco.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="f0bcb-121">Portanto, nenhum dois blocos consecutivos em uma enumeração teria o mesmo status de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="f0bcb-122">Esses blocos não se sobrepõem no tempo.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="f0bcb-123">Quando há itens sobrepostos em um calendário, o Outlook mescla esses itens para formar blocos de disponibilidade não sobrepostos na enumeração com base nesta ordem de prioridade: ausência temporária, ocupado, provisório.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="f0bcb-124">Para registrar o provedor de disponibilidade com o Outlook, o provedor de email deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f0bcb-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="f0bcb-125">Registre o provedor de disponibilidade com com, fornecendo um CLSID que permite o acesso à implementação do **IFreeBusySupport**do provedor.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="f0bcb-126">Deixe o Outlook saber que existe o provedor de disponibilidade, definindo a seguinte chave (onde `<xx.x>` representa a versão do Outlook) no registro do sistema:</span><span class="sxs-lookup"><span data-stu-id="f0bcb-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="f0bcb-127">Por exemplo, se o provedor de transporte for SMTP, para registrar o provedor com o Microsoft Outlook 2010, defina a seguinte chave como os dados na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="f0bcb-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="f0bcb-128">Nome</span><span class="sxs-lookup"><span data-stu-id="f0bcb-128">Name</span></span> |<span data-ttu-id="f0bcb-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0bcb-129">Type</span></span> |<span data-ttu-id="f0bcb-130">Valor</span><span class="sxs-lookup"><span data-stu-id="f0bcb-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="f0bcb-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="f0bcb-131">SMTP</span></span>  |<span data-ttu-id="f0bcb-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f0bcb-132">REG_SZ</span></span>  |<span data-ttu-id="f0bcb-133">{CLSID para a respectiva implementação de IFreeBusySupport}</span><span class="sxs-lookup"><span data-stu-id="f0bcb-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="f0bcb-134">Neste cenário, o Outlook cria a classe COM e a usa para recuperar as informações de disponibilidade de qualquer usuário de email SMTP.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="f0bcb-135">Para dar suporte a um catálogo de endereços e um provedor de transporte que usam um tipo de entrada de endereço diferente de SMTP, altere o *nome* de acordo.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f0bcb-136">Durante a instalação, os provedores de disponibilidade devem verificar se uma configuração de registro para o mesmo tipo de entrada de endereço já existe.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="f0bcb-137">Se isso acontecer, o provedor de disponibilidade deverá substituir o provedor atual por esse tipo de entrada de endereço e restaurá-lo ao provedor quando ele for desinstalado.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="f0bcb-138">No enTanto, se um usuário tiver instalado mais de um provedor de disponibilidade para o mesmo tipo de entrada de endereço, o usuário deverá desinstalar esses provedores na ordem inversa como instalação (ou seja, sempre desinstalar o provedor mais recente).</span><span class="sxs-lookup"><span data-stu-id="f0bcb-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="f0bcb-139">Caso contrário, o registro pode apontar para um provedor que já foi desinstalado.</span><span class="sxs-lookup"><span data-stu-id="f0bcb-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="f0bcb-140">Componentes da API</span><span class="sxs-lookup"><span data-stu-id="f0bcb-140">API components</span></span>

<span data-ttu-id="f0bcb-141">A API de disponibilidade inclui os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="f0bcb-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="f0bcb-142">Definições</span><span class="sxs-lookup"><span data-stu-id="f0bcb-142">Definitions</span></span>

- [<span data-ttu-id="f0bcb-143">Constantes (API do serviço de disponibilidade)</span><span class="sxs-lookup"><span data-stu-id="f0bcb-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="f0bcb-144">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="f0bcb-144">Data types</span></span>

- [<span data-ttu-id="f0bcb-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="f0bcb-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="f0bcb-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="f0bcb-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="f0bcb-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="f0bcb-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="f0bcb-148">Interfaces</span><span class="sxs-lookup"><span data-stu-id="f0bcb-148">Interfaces</span></span>

- [<span data-ttu-id="f0bcb-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="f0bcb-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="f0bcb-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="f0bcb-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="f0bcb-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="f0bcb-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

