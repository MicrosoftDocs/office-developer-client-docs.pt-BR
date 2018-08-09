---
title: Gravar um cliente automatizado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e5357c1e822dda35d3f38e00f91b58adbaf0ff9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770717"
---
# <a name="writing-an-automated-client"></a><span data-ttu-id="68b1e-103">Gravar um cliente automatizado</span><span class="sxs-lookup"><span data-stu-id="68b1e-103">Writing an Automated Client</span></span>

  
  
<span data-ttu-id="68b1e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68b1e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68b1e-105">Um aplicativo cliente automatizado é um aplicativo que executa autônomo, não exibindo nenhuma interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="68b1e-105">An automated client application is an application that runs unattended, displaying no user interface.</span></span>
  
 <span data-ttu-id="68b1e-106">Por padrão, muitos métodos de interface MAPI mostram uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="68b1e-106">By default, many MAPI interface methods show a user interface.</span></span> <span data-ttu-id="68b1e-107">Todos esses métodos têm os sinalizadores que permitem que um cliente permitir ou suprimir essa exibição.</span><span class="sxs-lookup"><span data-stu-id="68b1e-107">All of these methods have flags that allow a client to either allow or suppress this display.</span></span> <span data-ttu-id="68b1e-108">Embora o MAPI espera provedores de serviços para honram esses sinalizadores, existem alguns provedores que sempre não atendem a essas expectativas.</span><span class="sxs-lookup"><span data-stu-id="68b1e-108">Although MAPI expects service providers to honor these flags, there are some providers that do not always meet these expectations.</span></span> <span data-ttu-id="68b1e-109">Um motivo legítimo não respeitar os sinalizadores é a dependência do provedor de serviços em um outro serviço que não permita a supressão de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="68b1e-109">A legitimate reason for not honoring the flags is the reliance of the service provider on another service that does not allow user interface suppression.</span></span> <span data-ttu-id="68b1e-110">Se você estiver desenvolvendo um cliente automatizado, preste bastante atenção para os provedores de serviços que você está usando e como eles são configurados.</span><span class="sxs-lookup"><span data-stu-id="68b1e-110">If you are developing an automated client, pay careful attention to the service providers you are using and how they are configured.</span></span> <span data-ttu-id="68b1e-111">Não presuma que todas as suas chamadas a fim de suprimir uma interface de usuário poderão ser bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="68b1e-111">Do not assume that all of your calls to suppress a user interface will be successful.</span></span> 
  
<span data-ttu-id="68b1e-112">Clientes automatizados devem ter as informações necessárias para a configuração correta de cada um dos serviços de mensagem disponíveis no perfil.</span><span class="sxs-lookup"><span data-stu-id="68b1e-112">Automated clients must have the necessary information available for proper configuration of each of the message services in the profile.</span></span> <span data-ttu-id="68b1e-113">Há duas maneiras de fornecer informações de configuração no momento do logon:</span><span class="sxs-lookup"><span data-stu-id="68b1e-113">There are two ways to supply configuration information at logon time:</span></span>
  
- <span data-ttu-id="68b1e-114">O provedor de serviços pode recuperar informações do perfil.</span><span class="sxs-lookup"><span data-stu-id="68b1e-114">The service provider can retrieve information from the profile.</span></span>
    
- <span data-ttu-id="68b1e-115">O provedor de serviços pode solicitar informações do usuário.</span><span class="sxs-lookup"><span data-stu-id="68b1e-115">The service provider can prompt the user for information.</span></span> 
    
<span data-ttu-id="68b1e-116">Desde que a segunda opção não estiver disponível para os clientes automatizados, esses clientes devem usar a primeira opção.</span><span class="sxs-lookup"><span data-stu-id="68b1e-116">Since the second option is unavailable to automated clients, these clients must use the first option.</span></span> <span data-ttu-id="68b1e-117">Clientes devem configurar seus perfis cuidadosamente para garantir que esta opção sempre funciona.</span><span class="sxs-lookup"><span data-stu-id="68b1e-117">Clients must configure their profiles carefully to ensure that this option always works.</span></span>
  
<span data-ttu-id="68b1e-118">Clientes automatizados sempre defina o sinalizador MAPI_NO_MAIL na chamada da função [MAPILogonEx](mapilogonex.md) para iniciar uma sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="68b1e-118">Automated clients always set the MAPI_NO_MAIL flag in the [MAPILogonEx](mapilogonex.md) function call to begin a MAPI session.</span></span> 
  

