---
title: Instalar o subsistema MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Última modificação: 9 de março de 2015'
localization_priority: Priority
ms.openlocfilehash: 112a683f5967f8740c2d21285eb4ebbc0f455c48
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722435"
---
# <a name="installing-the-mapi-subsystem"></a><span data-ttu-id="df387-103">Instalar o subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="df387-103">Installing the MAPI Subsystem</span></span>

  
  
<span data-ttu-id="df387-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df387-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df387-105">As versões com suporte do Windows instalam a biblioteca stub do MAPI, Mapi32.dll, na pasta  _\<drive\>_ \Windows\System32.</span><span class="sxs-lookup"><span data-stu-id="df387-105">Supported versions of Windows install the MAPI stub library, Mapi32.dll, in the  _\<drive\>_ \Windows\System32 folder.</span></span> 
  
<span data-ttu-id="df387-106">As versões com suporte do Windows são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="df387-106">The supported versions of Windows are as follows:</span></span>
  
- <span data-ttu-id="df387-107">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="df387-107">Windows 7</span></span>
    
- <span data-ttu-id="df387-108">Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="df387-108">Windows Vista</span></span>
    
- <span data-ttu-id="df387-109">Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="df387-109">Windows Server 2008</span></span>
    
- <span data-ttu-id="df387-110">Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="df387-110">Windows Server 2003</span></span>
    
- <span data-ttu-id="df387-111">Windows XP.</span><span class="sxs-lookup"><span data-stu-id="df387-111">Windows XP</span></span>
    
<span data-ttu-id="df387-112">Para instalar corretamente o subsistema MAPI, instale um aplicativo que contenha um subsistema baseado em MAPI, como o Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="df387-112">To correctly install the MAPI subsystem, install an application that contains a MAPI-based subsystem, such as Microsoft Outlook.</span></span>
  
<span data-ttu-id="df387-113">Você pode encontrar informações sobre a instalação de subsistema MAPI do computador no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="df387-113">You can find information about a computer's MAPI subsystem installation in the system registry.</span></span> <span data-ttu-id="df387-114">Todos os valores das entradas de registro são cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="df387-114">All values in the registry entries are character strings.</span></span> 
  
<span data-ttu-id="df387-115">Os programas de instalação do serviço de mensagens são responsáveis por criar as informações de instalação na seguinte chave de registro do sistema:</span><span class="sxs-lookup"><span data-stu-id="df387-115">Message service installation programs are responsible for creating the installation information in the following system registry key:</span></span> 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
<span data-ttu-id="df387-116">Os serviços de mensagem devem adicionar entradas ao registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="df387-116">Message services must add entries to the system registry.</span></span> 
  
<span data-ttu-id="df387-117">A tabela a seguir resume a forma como os clientes recuperam informações de versão para o subsistema MAPI em seus computadores.</span><span class="sxs-lookup"><span data-stu-id="df387-117">The following table summarizes how clients retrieve version information for the MAPI subsystem on their computer.</span></span>
  
|<span data-ttu-id="df387-118">**Para verificar**</span><span class="sxs-lookup"><span data-stu-id="df387-118">**To check**</span></span>|<span data-ttu-id="df387-119">**Registro**</span><span class="sxs-lookup"><span data-stu-id="df387-119">**Registry**</span></span>|
|:-----|:-----|
|<span data-ttu-id="df387-120">Disponibilidade de MAPI</span><span class="sxs-lookup"><span data-stu-id="df387-120">Availability of MAPI</span></span>  <br/> |<span data-ttu-id="df387-121">Procure  `MAPIX=1`.</span><span class="sxs-lookup"><span data-stu-id="df387-121">Look for  `MAPIX=1`.</span></span>  <br/> |
|<span data-ttu-id="df387-122">Versão de MAPI disponível</span><span class="sxs-lookup"><span data-stu-id="df387-122">Available version of MAPI</span></span>  <br/> |<span data-ttu-id="df387-123">Procure uma cadeia de caracteres MAPIXVER do formulário " _x.x.x_".</span><span class="sxs-lookup"><span data-stu-id="df387-123">Look for a MAPIXVER string of the form " _x.x.x_".</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df387-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="df387-124">See also</span></span>



[<span data-ttu-id="df387-125">Visão geral da programação MAPI</span><span class="sxs-lookup"><span data-stu-id="df387-125">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

