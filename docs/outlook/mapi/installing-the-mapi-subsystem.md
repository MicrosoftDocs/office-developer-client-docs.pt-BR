---
title: Instalando o subsistema de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: c2e135fc031dd3faf5a4e08c50147dfcf7787b5e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767562"
---
# <a name="installing-the-mapi-subsystem"></a><span data-ttu-id="30ae3-103">Instalando o subsistema de MAPI</span><span class="sxs-lookup"><span data-stu-id="30ae3-103">Installing the MAPI Subsystem</span></span>

  
  
<span data-ttu-id="30ae3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30ae3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30ae3-105">Versões suportadas do Windows instalem a biblioteca de stub MAPI, Mapi32, no _ \<unidade\>_ \Windows\System32 folder.</span><span class="sxs-lookup"><span data-stu-id="30ae3-105">Supported versions of Windows install the MAPI stub library, Mapi32.dll, in the  _\<drive\>_ \Windows\System32 folder.</span></span> 
  
<span data-ttu-id="30ae3-106">As versões com suporte do Windows são:</span><span class="sxs-lookup"><span data-stu-id="30ae3-106">The supported versions of Windows are as follows:</span></span>
  
- <span data-ttu-id="30ae3-107">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="30ae3-107">Windows 7.</span></span>
    
- <span data-ttu-id="30ae3-108">Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="30ae3-108">Windows Vista.</span></span>
    
- <span data-ttu-id="30ae3-109">Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="30ae3-109">Windows Server 2008.</span></span>
    
- <span data-ttu-id="30ae3-110">Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="30ae3-110">Windows Server 2003.</span></span>
    
- <span data-ttu-id="30ae3-111">Windows XP.</span><span class="sxs-lookup"><span data-stu-id="30ae3-111">Windows XP.</span></span>
    
<span data-ttu-id="30ae3-112">Para instalar corretamente o subsistema de MAPI, instale um aplicativo que contém um subsistema baseado em MAPI, como o Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="30ae3-112">To correctly install the MAPI subsystem, install an application that contains a MAPI-based subsystem, such as Microsoft Outlook.</span></span>
  
<span data-ttu-id="30ae3-113">Você pode encontrar informações sobre a instalação do subsistema MAPI do computador no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="30ae3-113">You can find information about a computer's MAPI subsystem installation in the system registry.</span></span> <span data-ttu-id="30ae3-114">Todos os valores nas entradas de registro são cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="30ae3-114">All values in the registry entries are character strings.</span></span> 
  
<span data-ttu-id="30ae3-115">Programas de instalação do serviço de mensagem são responsáveis por criar as informações de instalação na seguinte chave de registro do sistema:</span><span class="sxs-lookup"><span data-stu-id="30ae3-115">Message service installation programs are responsible for creating the installation information in the following system registry key:</span></span> 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
<span data-ttu-id="30ae3-116">Serviços de mensagem devem adicionar entradas do registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="30ae3-116">Message services must add entries to the system registry.</span></span> 
  
<span data-ttu-id="30ae3-117">A tabela a seguir resume como clientes recuperam informações de versão para o subsistema MAPI em seus computadores.</span><span class="sxs-lookup"><span data-stu-id="30ae3-117">The following table summarizes how clients retrieve version information for the MAPI subsystem on their computer.</span></span>
  
|<span data-ttu-id="30ae3-118">**Para verificar**</span><span class="sxs-lookup"><span data-stu-id="30ae3-118">**To check**</span></span>|<span data-ttu-id="30ae3-119">**Registry**</span><span class="sxs-lookup"><span data-stu-id="30ae3-119">**Registry**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30ae3-120">Disponibilidade de MAPI</span><span class="sxs-lookup"><span data-stu-id="30ae3-120">Availability of MAPI</span></span>  <br/> |<span data-ttu-id="30ae3-121">Procure por `MAPIX=1`.</span><span class="sxs-lookup"><span data-stu-id="30ae3-121">Look for  `MAPIX=1`.</span></span>  <br/> |
|<span data-ttu-id="30ae3-122">Versão disponível de MAPI</span><span class="sxs-lookup"><span data-stu-id="30ae3-122">Available version of MAPI</span></span>  <br/> |<span data-ttu-id="30ae3-123">Procure por uma cadeia de caracteres MAPIXVER do formulário " _x.x.x_".</span><span class="sxs-lookup"><span data-stu-id="30ae3-123">Look for a MAPIXVER string of the form " _x.x.x_".</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30ae3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="30ae3-124">See also</span></span>



[<span data-ttu-id="30ae3-125">Vis�o geral da programa��o MAPI</span><span class="sxs-lookup"><span data-stu-id="30ae3-125">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

