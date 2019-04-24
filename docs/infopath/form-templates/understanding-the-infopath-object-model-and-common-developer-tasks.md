---
title: Noções básicas sobre o modelo de objeto do InfoPath e tarefas comuns de desenvolvedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- exemplos [InfoPath 2007], InfoPath 2007, tarefas de desenvolvedor, tarefas de desenvolvedor [InfoPath 2007], InfoPath 2007, modelos de objeto, modelos de objeto [InfoPath 2007]
localization_priority: Normal
ms.assetid: a2c18b72-426b-4f63-8454-187e96d26199
description: Esta seção fornece informações sobre tarefas comuns de desenvolvedor ao desenvolver modelos de formulário de código gerenciado do InfoPath.
ms.openlocfilehash: a84bf1a70407ca87e1a83f74856d363d8860d4a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303434"
---
# <a name="understanding-the-infopath-object-model-and-common-developer-tasks"></a><span data-ttu-id="d59e4-104">Noções básicas sobre o modelo de objeto do InfoPath e tarefas comuns de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="d59e4-104">Understanding the InfoPath Object Model and Common Developer Tasks</span></span>

<span data-ttu-id="d59e4-105">Esta seção fornece informações sobre tarefas comuns de desenvolvedor ao desenvolver modelos de formulário de código gerenciado do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d59e4-105">This section provides information on common developer tasks when developing InfoPath managed code form templates.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="d59e4-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d59e4-106">In this section</span></span>

[<span data-ttu-id="d59e4-107">Acessar dados de aplicativo</span><span class="sxs-lookup"><span data-stu-id="d59e4-107">Access Application Data</span></span>](how-to-access-application-data.md)
  
> <span data-ttu-id="d59e4-108">Descreve como acessar informações sobre o aplicativo do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d59e4-108">Discusses how to access information about the InfoPath application.</span></span>
    
[<span data-ttu-id="d59e4-109">Responder a eventos de formulário</span><span class="sxs-lookup"><span data-stu-id="d59e4-109">Respond to Form Events</span></span>](how-to-respond-to-form-events.md)
  
> <span data-ttu-id="d59e4-110">Descreve como criar manipuladores de eventos que respondem a eventos que ocorrem quando um usuário preenche um formulário.</span><span class="sxs-lookup"><span data-stu-id="d59e4-110">Discusses how to create event handlers that respond to events that occur as a user fills out a form.</span></span>
    
[<span data-ttu-id="d59e4-111">Acessar dados de formulário</span><span class="sxs-lookup"><span data-stu-id="d59e4-111">Access Form Data</span></span>](how-to-access-form-data.md)
  
> <span data-ttu-id="d59e4-112">Descreve como acessar informações sobre o documento XML subjacente do formulário, os dados que ele contém ou para executar alguma ação no documento XML.</span><span class="sxs-lookup"><span data-stu-id="d59e4-112">Discusses how to access information about the form's underlying XML document, the data it contains, or to perform some action on the XML document.</span></span>
    
[<span data-ttu-id="d59e4-113">Acessar fontes de dados externas</span><span class="sxs-lookup"><span data-stu-id="d59e4-113">Access External Data Sources</span></span>](how-to-access-external-data-sources.md)
  
> <span data-ttu-id="d59e4-114">Descreve como acessar dados de fontes de dados externas.</span><span class="sxs-lookup"><span data-stu-id="d59e4-114">Discusses how to access data from external data sources.</span></span>
    
[<span data-ttu-id="d59e4-115">Gravar lógica condicional que determina o ambiente de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="d59e4-115">Write Conditional Logic That Determines the Run-time Environment</span></span>](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
> <span data-ttu-id="d59e4-116">Discute como escrever código que executa uma ação diferente dependendo se o formulário está aberto no InfoPath, em um navegador da Web ou em um navegador móvel.</span><span class="sxs-lookup"><span data-stu-id="d59e4-116">Discusses how to write code that performs a different action depending on whether the form is open in InfoPath, a Web browser, or a mobile browser.</span></span>
    
[<span data-ttu-id="d59e4-117">Trabalhar com janelas de formulários</span><span class="sxs-lookup"><span data-stu-id="d59e4-117">Work with Form Windows</span></span>](how-to-work-with-form-windows.md)
  
> <span data-ttu-id="d59e4-118">Discute como trabalhar com janelas de formulários.</span><span class="sxs-lookup"><span data-stu-id="d59e4-118">Discusses how to work with form windows.</span></span>
    
[<span data-ttu-id="d59e4-119">Trabalhar com modos de exibição</span><span class="sxs-lookup"><span data-stu-id="d59e4-119">Work with Views</span></span>](how-to-work-with-views.md)
  
> <span data-ttu-id="d59e4-120">Discute como trabalhar com modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="d59e4-120">Discusses how to work with views.</span></span>
    
[<span data-ttu-id="d59e4-121">Trabalhar com soluções offline</span><span class="sxs-lookup"><span data-stu-id="d59e4-121">Work with Offline Solutions</span></span>](how-to-work-with-offline-solutions.md)
  
> <span data-ttu-id="d59e4-122">Discute como trabalhar com soluções offline.</span><span class="sxs-lookup"><span data-stu-id="d59e4-122">Discusses how to work with offline solutions.</span></span>
    
[<span data-ttu-id="d59e4-123">Trabalhar com assinaturas digitais</span><span class="sxs-lookup"><span data-stu-id="d59e4-123">Work with Digital Signatures</span></span>](how-to-work-with-digital-signatures.md)
  
> <span data-ttu-id="d59e4-124">Discute como trabalhar com assinaturas digitais.</span><span class="sxs-lookup"><span data-stu-id="d59e4-124">Discusses how to work with digital signatures.</span></span>
    
[<span data-ttu-id="d59e4-125">Manipular erros</span><span class="sxs-lookup"><span data-stu-id="d59e4-125">Handle Errors</span></span>](how-to-handle-errors.md)
  
> <span data-ttu-id="d59e4-126">Descreve como lidar com erros nos projetos de código gerenciado do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d59e4-126">Discusses how to handle errors in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="d59e4-127">Trabalhar com configurações de gerenciamento de direitos de informação</span><span class="sxs-lookup"><span data-stu-id="d59e4-127">Work with Information Rights Management Settings</span></span>](how-to-work-with-information-rights-management-settings.md)
  
> <span data-ttu-id="d59e4-128">Descreve como trabalhar com as configurações do gerenciamento de direitos de informação (IRM).</span><span class="sxs-lookup"><span data-stu-id="d59e4-128">Discusses how to work with Information Rights Management (IRM) settings.</span></span>
    
[<span data-ttu-id="d59e4-129">Adicionar e fazer referência a assemblies personalizados</span><span class="sxs-lookup"><span data-stu-id="d59e4-129">Add and Reference Custom Assemblies</span></span>](how-to-add-and-reference-custom-assemblies.md)
  
> <span data-ttu-id="d59e4-130">Discute como adicionar assemblies personalizados a um projeto de modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="d59e4-130">Discusses how to add custom assemblies to a form template project.</span></span>
    

