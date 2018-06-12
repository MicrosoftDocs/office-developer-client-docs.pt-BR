---
title: Sobre a API de livre/ocupado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: A API de Free/Busy permite que os provedores de email fornecer informações de status livre/ocupado para contas de usuário especificado dentro de um intervalo de tempo especificado.
ms.openlocfilehash: 8b1559173297fbde9930b6f8f7fbc74f176273da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765792"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="2db5a-103">Sobre a API de livre/ocupado</span><span class="sxs-lookup"><span data-stu-id="2db5a-103">About the Free/Busy API</span></span>

<span data-ttu-id="2db5a-104">A API de Free/Busy permite que os provedores de email fornecer informações de status livre/ocupado para contas de usuário especificado dentro de um intervalo de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="2db5a-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="2db5a-105">O status livre/ocupado de um bloco de horário no calendário do usuário é um dos seguintes: fora do escritório, ocupado, provisório ou livre.</span><span class="sxs-lookup"><span data-stu-id="2db5a-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="2db5a-106">Criar um provedor de livre/ocupado</span><span class="sxs-lookup"><span data-stu-id="2db5a-106">Create a free/busy provider</span></span>

<span data-ttu-id="2db5a-107">Para fornecer informações de livre/ocupado para usuários de email, um provedor de email cria um provedor de livre/ocupado e registra-lo com o Outlook.</span><span class="sxs-lookup"><span data-stu-id="2db5a-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="2db5a-108">O provedor de livre/ocupado deve implementar estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="2db5a-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="2db5a-109">Observe que um número de membros nessas interfaces não é suportado e deve retornar que valores de retorno especificado.</span><span class="sxs-lookup"><span data-stu-id="2db5a-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="2db5a-110">Especificamente, a API Free/Busy não oferece suporte para acesso de gravação para as informações de disponibilidade e delegar acesso às contas.</span><span class="sxs-lookup"><span data-stu-id="2db5a-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="2db5a-111">[IFreeBusySupport](ifreebusysupport.md) — essa interface suporta a especificação das interfaces que acessam dados livre/ocupado para usuários especificados.</span><span class="sxs-lookup"><span data-stu-id="2db5a-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="2db5a-112">Ele usa [FBUser](fbuser.md) para identificar um usuário.</span><span class="sxs-lookup"><span data-stu-id="2db5a-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="2db5a-113">[IFreeBusyData](ifreebusydata.md) — essa interface obtém e define um intervalo de tempo para um determinado usuário e retorna uma interface para enumerar os blocos de informações de disponibilidade de dados dentro deste intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="2db5a-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="2db5a-114">Ele usa o tempo relativo para obter e definir esse intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="2db5a-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="2db5a-115">Para obter mais informações, consulte [tempo relativo para acessar informações de disponibilidade de dados de uso](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="2db5a-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="2db5a-116">[IEnumFBBlock](ienumfbblock.md) — essa interface suporta acessando e enumerando blocos de informações de disponibilidade de dados de um usuário em um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="2db5a-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="2db5a-117">Uma enumeração contém blocos de livre/ocupado que indicam o status livre/ocupado de períodos de tempo no calendário do usuário, dentro de um intervalo de tempo (especificado por [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span><span class="sxs-lookup"><span data-stu-id="2db5a-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="2db5a-118">Itens em um calendário, como compromissos e solicitações de reunião, blocos de formulário na enumeração.</span><span class="sxs-lookup"><span data-stu-id="2db5a-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="2db5a-119">Itens que são adjacentes uns aos outros no calendário e têm o mesmo status livre/ocupado são combinados para um único bloco do formulário.</span><span class="sxs-lookup"><span data-stu-id="2db5a-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="2db5a-120">Um período livre de tempo em um calendário também um bloco de formulários.</span><span class="sxs-lookup"><span data-stu-id="2db5a-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="2db5a-121">Portanto, não há dois blocos consecutivos em uma enumeração teria o mesmo status livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="2db5a-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="2db5a-122">Esses blocos não se sobreponham em tempo.</span><span class="sxs-lookup"><span data-stu-id="2db5a-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="2db5a-123">Quando houver sobreposição de itens em um calendário, o Outlook mescla desses itens para formar não sobrepostos blocos de livre/ocupado na enumeração com base nesta ordem de precedência: fora do escritório, ocupado, provisório.</span><span class="sxs-lookup"><span data-stu-id="2db5a-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="2db5a-124">Para registrar o provedor de informações de disponibilidade com o Outlook, o provedor de email deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2db5a-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="2db5a-125">Registre o provedor de livre/ocupado com, fornecendo um CLSID que permite o acesso a implementação do provedor de **IFreeBusySupport**.</span><span class="sxs-lookup"><span data-stu-id="2db5a-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="2db5a-126">Permitir que o Outlook saibam a existência de provedor de livre/ocupado, definindo a seguinte chave (onde `<xx.x>` representa a versão do Outlook) no registro do sistema:</span><span class="sxs-lookup"><span data-stu-id="2db5a-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="2db5a-127">Por exemplo, se o provedor de transporte for SMTP, para registrar o provedor com o Microsoft Outlook 2010, defina a seguinte chave para os dados na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="2db5a-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="2db5a-128">Name</span><span class="sxs-lookup"><span data-stu-id="2db5a-128">Name</span></span> |<span data-ttu-id="2db5a-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2db5a-129">Type</span></span> |<span data-ttu-id="2db5a-130">Value</span><span class="sxs-lookup"><span data-stu-id="2db5a-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="2db5a-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="2db5a-131">SMTP</span></span>  |<span data-ttu-id="2db5a-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2db5a-132">REG_SZ</span></span>  |<span data-ttu-id="2db5a-133">{CLSID referente a respectiva implementação da IFreeBusySupport}</span><span class="sxs-lookup"><span data-stu-id="2db5a-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="2db5a-134">Neste cenário, o Outlook co cria a classe COM e o utiliza para recuperar informações de disponibilidade para os usuários de email SMTP.</span><span class="sxs-lookup"><span data-stu-id="2db5a-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="2db5a-135">Para oferecer suporte a um provedor de transporte e o catálogo de endereço que usam um tipo de endereço de entrada que não seja o SMTP, altere o *nome* de acordo.</span><span class="sxs-lookup"><span data-stu-id="2db5a-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2db5a-136">Durante a instalação, provedores de livre/ocupado devem verificar se uma configuração de registro para o mesmo tipo de entrada de endereço já existe.</span><span class="sxs-lookup"><span data-stu-id="2db5a-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="2db5a-137">Se contiver, o provedor de livre/ocupado deve substituir o provedor atual para esse tipo de entrada de endereço e restaure desse provedor quando ele é desinstalado.</span><span class="sxs-lookup"><span data-stu-id="2db5a-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="2db5a-138">No entanto, se um usuário tiver instalado mais de um provedor de livre/ocupado para o mesmo tipo de entrada de endereço, o usuário deve desinstalar esses provedores na ordem inversa da instalação (ou seja, desinstale sempre o provedor mais recente).</span><span class="sxs-lookup"><span data-stu-id="2db5a-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="2db5a-139">Caso contrário, o registro pode apontar para um provedor que já está desinstalado.</span><span class="sxs-lookup"><span data-stu-id="2db5a-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="2db5a-140">Componentes de API</span><span class="sxs-lookup"><span data-stu-id="2db5a-140">API components</span></span>

<span data-ttu-id="2db5a-141">A API Free/Busy inclui os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="2db5a-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="2db5a-142">Definições</span><span class="sxs-lookup"><span data-stu-id="2db5a-142">Definitions</span></span>

- [<span data-ttu-id="2db5a-143">Constantes (API de livre/ocupado)</span><span class="sxs-lookup"><span data-stu-id="2db5a-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="2db5a-144">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="2db5a-144">Data types</span></span>

- [<span data-ttu-id="2db5a-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="2db5a-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="2db5a-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="2db5a-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="2db5a-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="2db5a-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="2db5a-148">Interfaces</span><span class="sxs-lookup"><span data-stu-id="2db5a-148">Interfaces</span></span>

- [<span data-ttu-id="2db5a-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="2db5a-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="2db5a-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="2db5a-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="2db5a-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="2db5a-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

