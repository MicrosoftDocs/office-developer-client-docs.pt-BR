---
title: Gravar um cliente automatizado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f9ce3452bbc2d3297cc67168835a9387235746a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439762"
---
# <a name="writing-an-automated-client"></a><span data-ttu-id="7e98c-103">Gravar um cliente automatizado</span><span class="sxs-lookup"><span data-stu-id="7e98c-103">Writing an Automated Client</span></span>

  
  
<span data-ttu-id="7e98c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e98c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e98c-105">Um aplicativo cliente automatizado é um aplicativo que executa o autônomo, não exibindo nenhuma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="7e98c-105">An automated client application is an application that runs unattended, displaying no user interface.</span></span>
  
 <span data-ttu-id="7e98c-106">Por padrão, muitos métodos de interface MAPI mostram uma interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="7e98c-106">By default, many MAPI interface methods show a user interface.</span></span> <span data-ttu-id="7e98c-107">Todos esses métodos têm sinalizadores que permitem que um cliente permita ou suprima essa exibição.</span><span class="sxs-lookup"><span data-stu-id="7e98c-107">All of these methods have flags that allow a client to either allow or suppress this display.</span></span> <span data-ttu-id="7e98c-108">Embora o MAPI espere que os provedores de serviços obedeçam a esses sinalizadores, há alguns provedores que nem sempre atendem a essas expectativas.</span><span class="sxs-lookup"><span data-stu-id="7e98c-108">Although MAPI expects service providers to honor these flags, there are some providers that do not always meet these expectations.</span></span> <span data-ttu-id="7e98c-109">Uma razão legítima para não honrar os sinalizadores é a confiança do provedor de serviços em outro serviço que não permite a supressão da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="7e98c-109">A legitimate reason for not honoring the flags is the reliance of the service provider on another service that does not allow user interface suppression.</span></span> <span data-ttu-id="7e98c-110">Se você estiver desenvolvendo um cliente automatizado, preste atenção cuidadosa aos provedores de serviços que está usando e como eles estão configurados.</span><span class="sxs-lookup"><span data-stu-id="7e98c-110">If you are developing an automated client, pay careful attention to the service providers you are using and how they are configured.</span></span> <span data-ttu-id="7e98c-111">Não presuma que todas as suas chamadas para suprimir uma interface do usuário serão bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="7e98c-111">Do not assume that all of your calls to suppress a user interface will be successful.</span></span> 
  
<span data-ttu-id="7e98c-112">Os clientes automatizados devem ter as informações necessárias disponíveis para a configuração adequada de cada um dos serviços de mensagens no perfil.</span><span class="sxs-lookup"><span data-stu-id="7e98c-112">Automated clients must have the necessary information available for proper configuration of each of the message services in the profile.</span></span> <span data-ttu-id="7e98c-113">Há duas maneiras de fornecer informações de configuração no momento do logon:</span><span class="sxs-lookup"><span data-stu-id="7e98c-113">There are two ways to supply configuration information at logon time:</span></span>
  
- <span data-ttu-id="7e98c-114">O provedor de serviços pode recuperar informações do perfil.</span><span class="sxs-lookup"><span data-stu-id="7e98c-114">The service provider can retrieve information from the profile.</span></span>
    
- <span data-ttu-id="7e98c-115">O provedor de serviços pode solicitar informações ao usuário.</span><span class="sxs-lookup"><span data-stu-id="7e98c-115">The service provider can prompt the user for information.</span></span> 
    
<span data-ttu-id="7e98c-116">Como a segunda opção não está disponível para clientes automatizados, esses clientes devem usar a primeira opção.</span><span class="sxs-lookup"><span data-stu-id="7e98c-116">Since the second option is unavailable to automated clients, these clients must use the first option.</span></span> <span data-ttu-id="7e98c-117">Os clientes devem configurar seus perfis com cuidado para garantir que essa opção funcione sempre.</span><span class="sxs-lookup"><span data-stu-id="7e98c-117">Clients must configure their profiles carefully to ensure that this option always works.</span></span>
  
<span data-ttu-id="7e98c-118">Os clientes automatizados sempre definem o sinalizador MAPI_NO_MAIL na chamada de função [funçãomapilogonex](mapilogonex.md) para iniciar uma sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="7e98c-118">Automated clients always set the MAPI_NO_MAIL flag in the [MAPILogonEx](mapilogonex.md) function call to begin a MAPI session.</span></span> 
  

