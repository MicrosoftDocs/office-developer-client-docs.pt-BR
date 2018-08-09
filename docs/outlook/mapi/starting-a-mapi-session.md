---
title: Iniciar sessão MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d683d5fc959b219569417c74494cb47d7c2c059e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770492"
---
# <a name="starting-a-mapi-session"></a><span data-ttu-id="966a7-103">Iniciar sessão MAPI</span><span class="sxs-lookup"><span data-stu-id="966a7-103">Starting a MAPI Session</span></span>

  
  
<span data-ttu-id="966a7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="966a7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="966a7-105">Embora não haja uma quantidade significativa de trabalho executado durante a sessão de inicialização, as tarefas necessárias são mínimas.</span><span class="sxs-lookup"><span data-stu-id="966a7-105">Although there is a significant amount of work performed during session start up, the required tasks are minimal.</span></span> <span data-ttu-id="966a7-106">Muito desse trabalho é feito de MAPI processamento das chamadas [MAPIInitialize](mapiinitialize.md) e [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="966a7-106">Much of this work is done in the MAPI processing of the [MAPIInitialize](mapiinitialize.md) and [MAPILogonEx](mapilogonex.md) calls.</span></span> <span data-ttu-id="966a7-107">Ambas as funções aceitam sinalizadores como parâmetros de entrada para controlar os aspectos da sessão como tratamento de notificação e a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="966a7-107">Both of these functions accept flags as input parameters for controlling aspects of the session such as notification handling and the user interface.</span></span> <span data-ttu-id="966a7-108">É importante entender as consequências de configuração de cada um desses sinalizadores ao chamar **MAPIInitialize** para inicializar as bibliotecas MAPI e **MAPILogonEx** para fazer logon no subsistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="966a7-108">It is important to understand the consequences of setting each of these flags when calling **MAPIInitialize** to initialize the MAPI libraries and **MAPILogonEx** to log on to the MAPI subsystem.</span></span> 
  
 <span data-ttu-id="966a7-109">**Para iniciar uma sessão MAPI**</span><span class="sxs-lookup"><span data-stu-id="966a7-109">**To start a MAPI session**</span></span>
  
1. <span data-ttu-id="966a7-110">Chame **MAPIInitialize** para inicializar o conjunto padrão de bibliotecas MAPI.</span><span class="sxs-lookup"><span data-stu-id="966a7-110">Call **MAPIInitialize** to initialize the standard set of MAPI libraries.</span></span> 
    
2. <span data-ttu-id="966a7-111">Se você precisa usar as bibliotecas OLE, chamar a função OLE [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="966a7-111">If you need to use the OLE libraries, call the OLE function [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span></span>
    
3. <span data-ttu-id="966a7-112">Se você precisar usar a biblioteca do utilitário MAPI, chame [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="966a7-112">If you need to use the MAPI utility library, call [ScInitMapiUtil](scinitmapiutil.md).</span></span>
    
4. <span data-ttu-id="966a7-113">Chame **MAPILogonEx** com um perfil válido para fazer logon no subsistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="966a7-113">Call **MAPILogonEx** with a valid profile to log on to the MAPI subsystem.</span></span> <span data-ttu-id="966a7-114">**MAPILogonEx** verifica a configuração de cada um dos provedores de serviço nos serviços de mensagem incluídos no perfil, avisar o usuário para obter informações adicionais, se necessário e possíveis.</span><span class="sxs-lookup"><span data-stu-id="966a7-114">**MAPILogonEx** verifies the configuration of each of the service providers in the message services included in the profile, prompting the user for additional information if necessary and possible.</span></span> <span data-ttu-id="966a7-115">Quando terminar de **MAPILogonEx** , os provedores de serviço configurado estão prontos para o serviço.</span><span class="sxs-lookup"><span data-stu-id="966a7-115">When **MAPILogonEx** completes, the configured service providers are ready for service.</span></span> 
    
## <a name="in-this-section"></a><span data-ttu-id="966a7-116">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="966a7-116">In this section</span></span>

[<span data-ttu-id="966a7-117">Iniciar MAPI</span><span class="sxs-lookup"><span data-stu-id="966a7-117">Initializing MAPI</span></span>](initializing-mapi.md)
  
> <span data-ttu-id="966a7-118">Descreve como inicializar MAPI para uma sessão.</span><span class="sxs-lookup"><span data-stu-id="966a7-118">Describes how to initialize MAPI for a session.</span></span>
    
[<span data-ttu-id="966a7-119">Iniciar OLE para MAPI</span><span class="sxs-lookup"><span data-stu-id="966a7-119">Initializing OLE for MAPI</span></span>](initializing-ole-for-mapi.md)
  
> <span data-ttu-id="966a7-120">Descreve as chamadas para fazer para inicializar o OLE para uso com MAPI.</span><span class="sxs-lookup"><span data-stu-id="966a7-120">Describes the calls to make to initialize OLE for use with MAPI.</span></span>
    
[<span data-ttu-id="966a7-121">Iniciar utilitários MAPI</span><span class="sxs-lookup"><span data-stu-id="966a7-121">Initializing the MAPI Utilities</span></span>](initializing-the-mapi-utilities.md)
  
> <span data-ttu-id="966a7-122">Descreve como inicializar utilitários MAPI.</span><span class="sxs-lookup"><span data-stu-id="966a7-122">Describes how to initialize MAPI utilities.</span></span>
    
[<span data-ttu-id="966a7-123">Fazer logon no MAPI</span><span class="sxs-lookup"><span data-stu-id="966a7-123">Logging on to MAPI</span></span>](logging-on-to-mapi.md)
  
> <span data-ttu-id="966a7-124">Descreve como aplicativos cliente faça logon no sistema de sub MAPI.</span><span class="sxs-lookup"><span data-stu-id="966a7-124">Describes how client applications log on to the MAPI sub system.</span></span>
    
