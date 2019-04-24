---
title: Iniciar uma sessão MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d88ce382b6a6b5f98ec5f88c4deb1565d3b60151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336341"
---
# <a name="starting-a-mapi-session"></a><span data-ttu-id="44c3b-103">Iniciar uma sessão MAPI</span><span class="sxs-lookup"><span data-stu-id="44c3b-103">Starting a MAPI Session</span></span>

  
  
<span data-ttu-id="44c3b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44c3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44c3b-105">Embora haja uma quantidade significativa de trabalho executado durante a inicialização da sessão, as tarefas necessárias são mínimas.</span><span class="sxs-lookup"><span data-stu-id="44c3b-105">Although there is a significant amount of work performed during session start up, the required tasks are minimal.</span></span> <span data-ttu-id="44c3b-106">Grande parte desse trabalho é feita no processamento de MAPI das chamadas [MAPIInitialize](mapiinitialize.md) e [funçãomapilogonex](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="44c3b-106">Much of this work is done in the MAPI processing of the [MAPIInitialize](mapiinitialize.md) and [MAPILogonEx](mapilogonex.md) calls.</span></span> <span data-ttu-id="44c3b-107">Ambas as funções aceitam sinalizadores como parâmetros de entrada para controlar os aspectos da sessão, como tratamento de notificações e a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="44c3b-107">Both of these functions accept flags as input parameters for controlling aspects of the session such as notification handling and the user interface.</span></span> <span data-ttu-id="44c3b-108">É importante entender as conseqüências da configuração de cada um desses sinalizadores ao chamar **MAPIInitialize** para inicializar as bibliotecas MAPI e o **funçãomapilogonex** para fazer logon no subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="44c3b-108">It is important to understand the consequences of setting each of these flags when calling **MAPIInitialize** to initialize the MAPI libraries and **MAPILogonEx** to log on to the MAPI subsystem.</span></span> 
  
 <span data-ttu-id="44c3b-109">**Para iniciar uma sessão MAPI**</span><span class="sxs-lookup"><span data-stu-id="44c3b-109">**To start a MAPI session**</span></span>
  
1. <span data-ttu-id="44c3b-110">Chame **MAPIInitialize** para inicializar o conjunto padrão de bibliotecas MAPI.</span><span class="sxs-lookup"><span data-stu-id="44c3b-110">Call **MAPIInitialize** to initialize the standard set of MAPI libraries.</span></span> 
    
2. <span data-ttu-id="44c3b-111">Se você precisar usar as bibliotecas OLE, chame a função OLE [OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="44c3b-111">If you need to use the OLE libraries, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span></span>
    
3. <span data-ttu-id="44c3b-112">Se você precisar usar a biblioteca de utilitários MAPI, chame [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="44c3b-112">If you need to use the MAPI utility library, call [ScInitMapiUtil](scinitmapiutil.md).</span></span>
    
4. <span data-ttu-id="44c3b-113">Chame **funçãomapilogonex** com um perfil válido para fazer logon no subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="44c3b-113">Call **MAPILogonEx** with a valid profile to log on to the MAPI subsystem.</span></span> <span data-ttu-id="44c3b-114">**Funçãomapilogonex** verifica a configuração de cada provedor de serviços nos serviços de mensagens incluídos no perfil, solicitando ao usuário informações adicionais, se necessário.</span><span class="sxs-lookup"><span data-stu-id="44c3b-114">**MAPILogonEx** verifies the configuration of each of the service providers in the message services included in the profile, prompting the user for additional information if necessary and possible.</span></span> <span data-ttu-id="44c3b-115">Quando o **funçãomapilogonex** é concluído, os provedores de serviços configurados estão prontos para o serviço.</span><span class="sxs-lookup"><span data-stu-id="44c3b-115">When **MAPILogonEx** completes, the configured service providers are ready for service.</span></span> 
    
## <a name="in-this-section"></a><span data-ttu-id="44c3b-116">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="44c3b-116">In this section</span></span>

[<span data-ttu-id="44c3b-117">Iniciar MAPI</span><span class="sxs-lookup"><span data-stu-id="44c3b-117">Initializing MAPI</span></span>](initializing-mapi.md)
  
> <span data-ttu-id="44c3b-118">Descreve como inicializar o MAPI para uma sessão.</span><span class="sxs-lookup"><span data-stu-id="44c3b-118">Describes how to initialize MAPI for a session.</span></span>
    
[<span data-ttu-id="44c3b-119">Iniciar OLE para MAPI</span><span class="sxs-lookup"><span data-stu-id="44c3b-119">Initializing OLE for MAPI</span></span>](initializing-ole-for-mapi.md)
  
> <span data-ttu-id="44c3b-120">Descreve as chamadas a serem feitas para inicializar o OLE para uso com MAPI.</span><span class="sxs-lookup"><span data-stu-id="44c3b-120">Describes the calls to make to initialize OLE for use with MAPI.</span></span>
    
[<span data-ttu-id="44c3b-121">Inicializando os utilitários MAPI</span><span class="sxs-lookup"><span data-stu-id="44c3b-121">Initializing the MAPI Utilities</span></span>](initializing-the-mapi-utilities.md)
  
> <span data-ttu-id="44c3b-122">Descreve como inicializar utilitários MAPI.</span><span class="sxs-lookup"><span data-stu-id="44c3b-122">Describes how to initialize MAPI utilities.</span></span>
    
[<span data-ttu-id="44c3b-123">Fazer logon no MAPI</span><span class="sxs-lookup"><span data-stu-id="44c3b-123">Logging on to MAPI</span></span>](logging-on-to-mapi.md)
  
> <span data-ttu-id="44c3b-124">Descreve como os aplicativos cliente fazem logon no sub-sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="44c3b-124">Describes how client applications log on to the MAPI sub system.</span></span>
    

