---
title: Função RUNADDONWARGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251493
localization_priority: Normal
ms.assetid: c154413f-c366-a66b-94e3-ed71ad23f325
description: Executa a cadeia de caracteres e passa os argumentos da linha de comando para o programa como uma cadeia de caracteres.
ms.openlocfilehash: bc05a4480438875c348373059f57bf04f82c9eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408702"
---
# <a name="runaddonwargs-function"></a><span data-ttu-id="e5521-103">Função RUNADDONWARGS</span><span class="sxs-lookup"><span data-stu-id="e5521-103">RUNADDONWARGS Function</span></span>

<span data-ttu-id="e5521-104">Executa  _a cadeia_ de caracteres e passa os  _argumentos da_ linha de comando para o programa como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e5521-104">Runs  _string_ and passes the command line  _arguments_ to the program as a string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e5521-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5521-105">Syntax</span></span>

<span data-ttu-id="e5521-106">RUNADDONWARGS(" \*\* *string* \*\* "," \*\* *arguments* \*\* ")</span><span class="sxs-lookup"><span data-stu-id="e5521-106">RUNADDONWARGS(" \*\* *string* \*\* "," \*\* *arguments* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e5521-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5521-107">Parameters</span></span>

|<span data-ttu-id="e5521-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e5521-108">**Name**</span></span>|<span data-ttu-id="e5521-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="e5521-109">**Required/Optional**</span></span>|<span data-ttu-id="e5521-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e5521-110">**Data Type**</span></span>|<span data-ttu-id="e5521-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e5521-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e5521-112">_string_</span><span class="sxs-lookup"><span data-stu-id="e5521-112">_string_</span></span> <br/> |<span data-ttu-id="e5521-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e5521-113">Required</span></span>  <br/> |<span data-ttu-id="e5521-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e5521-114">**String**</span></span> <br/> | <span data-ttu-id="e5521-115">O nome de um complemento.</span><span class="sxs-lookup"><span data-stu-id="e5521-115">The name of an add-on.</span></span>  <br/> |
| <span data-ttu-id="e5521-116">_arguments_</span><span class="sxs-lookup"><span data-stu-id="e5521-116">_arguments_</span></span> <br/> |<span data-ttu-id="e5521-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e5521-117">Required</span></span>  <br/> |<span data-ttu-id="e5521-118">**String**</span><span class="sxs-lookup"><span data-stu-id="e5521-118">**String**</span></span> <br/> |<span data-ttu-id="e5521-119">Argumentos a serem passados para seu programa.</span><span class="sxs-lookup"><span data-stu-id="e5521-119">Arguments to pass to your program.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5521-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5521-120">Remarks</span></span>

<span data-ttu-id="e5521-121">Na prática,  _os argumentos devem_ ter 50 caracteres ou menos.</span><span class="sxs-lookup"><span data-stu-id="e5521-121">In practice,  _arguments_ should be 50 or fewer characters.</span></span> <span data-ttu-id="e5521-122">Utilize a função RUNADDONWARGS para vincular um programa, como um complemento, a uma célula, por exemplo Action ou Events.</span><span class="sxs-lookup"><span data-stu-id="e5521-122">Use the RUNADDONWARGS function to bind a program, such as an add-on, to a cell, for example, to an Action or Events cell.</span></span> 
  
<span data-ttu-id="e5521-123">A função RUNADDONWARGS somente executa complementos que sejam membros da coleção **Addons** do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e5521-123">The RUNADDONWARGS function can only run add-ons that are members of the application's **Addons** collection.</span></span> <span data-ttu-id="e5521-124">Para fazer parte dessa coleção, um complemento precisar ser um arquivo EXE ou VSL, ou seja:</span><span class="sxs-lookup"><span data-stu-id="e5521-124">To be present in that collection, an add-on must be an EXE file or VSL file that is:</span></span> 
  
- <span data-ttu-id="e5521-125">Instalado no caminho **Startup** ou **Addons** do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e5521-125">Installed in the application's **Startup** or **Addons** path.</span></span> 
    
- <span data-ttu-id="e5521-126">Adicionado de forma programática usando o método **Add** da coleção **Addons**.</span><span class="sxs-lookup"><span data-stu-id="e5521-126">Added programmatically by using the **Add** method of the **Addons** collection.</span></span> 
    
<span data-ttu-id="e5521-127">Para obter mais informações sobre a execução de códigos no Visio, consulte [Sobre configurações de segurança e execução de códigos no Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) nesta Referência da ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="e5521-127">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="e5521-p103">Em versões anteriores do Visio, essa função aparece como _RUNADDONWARGS. As versões 4.0 e posteriores do Visio aceitam os dois estilos.</span><span class="sxs-lookup"><span data-stu-id="e5521-p103">In earlier versions of Visio, this function appears as _RUNADDONWARGS. Visio application versions 4.0 and later accept either style.</span></span>
  
## <a name="example"></a><span data-ttu-id="e5521-130">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e5521-130">Example</span></span>

<span data-ttu-id="e5521-131">RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack")</span><span class="sxs-lookup"><span data-stu-id="e5521-131">RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack")</span></span> 
  
<span data-ttu-id="e5521-132">Iniciará o complemento Graphmkr.exe e passará o argumento /GraphMaker=Stack.</span><span class="sxs-lookup"><span data-stu-id="e5521-132">Launches the add-on Graphmkr.exe and passes it the argument /GraphMaker=Stack.</span></span> 
  

