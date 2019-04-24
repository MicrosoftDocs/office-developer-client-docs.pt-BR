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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309636"
---
# <a name="installing-the-mapi-subsystem"></a><span data-ttu-id="02db7-103">Instalar o subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="02db7-103">Installing the MAPI Subsystem</span></span>

  
  
<span data-ttu-id="02db7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02db7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02db7-105">As versões com suporte do Windows instalam a biblioteca stub do MAPI, Mapi32.dll, na pasta  _\<drive\>_ \Windows\System32.</span><span class="sxs-lookup"><span data-stu-id="02db7-105">Supported versions of Windows install the MAPI stub library, Mapi32.dll, in the  _\<drive\>_ \Windows\System32 folder.</span></span> 
  
<span data-ttu-id="02db7-106">As versões com suporte do Windows são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="02db7-106">The supported versions of Windows are as follows:</span></span>
  
- <span data-ttu-id="02db7-107">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02db7-107">Windows 7.</span></span>
    
- <span data-ttu-id="02db7-108">Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="02db7-108">Windows Vista.</span></span>
    
- <span data-ttu-id="02db7-109">Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="02db7-109">Windows Server 2008.</span></span>
    
- <span data-ttu-id="02db7-110">Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="02db7-110">Windows Server 2003.</span></span>
    
- <span data-ttu-id="02db7-111">Windows XP.</span><span class="sxs-lookup"><span data-stu-id="02db7-111">Windows XP.</span></span>
    
<span data-ttu-id="02db7-112">Para instalar corretamente o subsistema MAPI, instale um aplicativo que contenha um subsistema baseado em MAPI, como o Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="02db7-112">To correctly install the MAPI subsystem, install an application that contains a MAPI-based subsystem, such as Microsoft Outlook.</span></span>
  
<span data-ttu-id="02db7-113">Você pode encontrar informações sobre a instalação de subsistema MAPI do computador no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="02db7-113">You can find information about a computer's MAPI subsystem installation in the system registry.</span></span> <span data-ttu-id="02db7-114">Todos os valores das entradas de registro são cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="02db7-114">All values in the registry entries are character strings.</span></span> 
  
<span data-ttu-id="02db7-115">Os programas de instalação do serviço de mensagens são responsáveis por criar as informações de instalação na seguinte chave de registro do sistema:</span><span class="sxs-lookup"><span data-stu-id="02db7-115">Message service installation programs are responsible for creating the installation information in the following system registry key:</span></span> 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
<span data-ttu-id="02db7-116">Os serviços de mensagem devem adicionar entradas ao registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="02db7-116">Message services must add entries to the system registry.</span></span> 
  
<span data-ttu-id="02db7-117">A tabela a seguir resume a forma como os clientes recuperam informações de versão para o subsistema MAPI em seus computadores.</span><span class="sxs-lookup"><span data-stu-id="02db7-117">The following table summarizes how clients retrieve version information for the MAPI subsystem on their computer.</span></span>
  
|<span data-ttu-id="02db7-118">**Para verificar**</span><span class="sxs-lookup"><span data-stu-id="02db7-118">**To check**</span></span>|<span data-ttu-id="02db7-119">**Registro**</span><span class="sxs-lookup"><span data-stu-id="02db7-119">**Registry**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02db7-120">Disponibilidade de MAPI</span><span class="sxs-lookup"><span data-stu-id="02db7-120">Availability of MAPI</span></span>  <br/> |<span data-ttu-id="02db7-121">Procure  `MAPIX=1`.</span><span class="sxs-lookup"><span data-stu-id="02db7-121">Look for  `MAPIX=1`.</span></span>  <br/> |
|<span data-ttu-id="02db7-122">Versão de MAPI disponível</span><span class="sxs-lookup"><span data-stu-id="02db7-122">Available version of MAPI</span></span>  <br/> |<span data-ttu-id="02db7-123">Procure uma cadeia de caracteres MAPIXVER do formulário " _x.x.x_".</span><span class="sxs-lookup"><span data-stu-id="02db7-123">Look for a MAPIXVER string of the form " _x.x.x_".</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02db7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="02db7-124">See also</span></span>



[<span data-ttu-id="02db7-125">Visão geral da programação MAPI</span><span class="sxs-lookup"><span data-stu-id="02db7-125">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

