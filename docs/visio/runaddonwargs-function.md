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
description: Executa a cadeia de caracteres e passa os argumentos de linha de comando para o programa como uma cadeia de caracteres.
ms.openlocfilehash: 7bc05a0cbf32550d1e39bee39bec83101882cf19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772831"
---
# <a name="runaddonwargs-function"></a><span data-ttu-id="6586b-103">Função RUNADDONWARGS</span><span class="sxs-lookup"><span data-stu-id="6586b-103">RUNADDONWARGS Function</span></span>

<span data-ttu-id="6586b-104">Executa a _cadeia de caracteres_ e passa os _argumentos_ de linha de comando para o programa como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6586b-104">Runs  _string_ and passes the command line  _arguments_ to the program as a string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6586b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6586b-105">Syntax</span></span>

<span data-ttu-id="6586b-106">RUNADDONWARGS ("* * *cadeia de caracteres* * *","* * *argumentos* * *")</span><span class="sxs-lookup"><span data-stu-id="6586b-106">RUNADDONWARGS(" ** *string* ** "," ** *arguments* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6586b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6586b-107">Parameters</span></span>

|<span data-ttu-id="6586b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6586b-108">**Name**</span></span>|<span data-ttu-id="6586b-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="6586b-109">**Required/Optional**</span></span>|<span data-ttu-id="6586b-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="6586b-110">**Data Type**</span></span>|<span data-ttu-id="6586b-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6586b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6586b-112">_string_</span><span class="sxs-lookup"><span data-stu-id="6586b-112">_string_</span></span> <br/> |<span data-ttu-id="6586b-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6586b-113">Required</span></span>  <br/> |<span data-ttu-id="6586b-114">**String**</span><span class="sxs-lookup"><span data-stu-id="6586b-114">**String**</span></span> <br/> | <span data-ttu-id="6586b-115">O nome de um complemento.</span><span class="sxs-lookup"><span data-stu-id="6586b-115">The name of an add-on.</span></span>  <br/> |
| <span data-ttu-id="6586b-116">_argumentos_</span><span class="sxs-lookup"><span data-stu-id="6586b-116">_arguments_</span></span> <br/> |<span data-ttu-id="6586b-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6586b-117">Required</span></span>  <br/> |<span data-ttu-id="6586b-118">**String**</span><span class="sxs-lookup"><span data-stu-id="6586b-118">**String**</span></span> <br/> |<span data-ttu-id="6586b-119">Argumentos a serem passados para seu programa.</span><span class="sxs-lookup"><span data-stu-id="6586b-119">Arguments to pass to your program.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6586b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6586b-120">Remarks</span></span>

<span data-ttu-id="6586b-121">Na prática, os _argumentos_ devem ser 50 caracteres ou menos.</span><span class="sxs-lookup"><span data-stu-id="6586b-121">In practice,  _arguments_ should be 50 or fewer characters.</span></span> <span data-ttu-id="6586b-122">Use a função RUNADDONWARGS para vincular um programa, como um complemento, a uma célula, por exemplo, a uma célula Action ou Events.</span><span class="sxs-lookup"><span data-stu-id="6586b-122">Use the RUNADDONWARGS function to bind a program, such as an add-on, to a cell, for example, to an Action or Events cell.</span></span> 
  
<span data-ttu-id="6586b-p102">A função RUNADDONWARGS somente executa complementos que sejam membros da coleção **Addons** do aplicativo. Para fazer parte dessa coleção, um complemento precisar ser um arquivo EXE ou VSL, ou seja:</span><span class="sxs-lookup"><span data-stu-id="6586b-p102">The RUNADDONWARGS function can only run add-ons that are members of the application's **Addons** collection. To be present in that collection, an add-on must be an EXE file or VSL file that is:</span></span> 
  
- <span data-ttu-id="6586b-125">Instalado no caminho **Startup** ou **Addons** do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6586b-125">Installed in the application's **Startup** or **Addons** path.</span></span> 
    
- <span data-ttu-id="6586b-126">Adicionado de forma programática usando o método **Add** da coleção **Addons**.</span><span class="sxs-lookup"><span data-stu-id="6586b-126">Added programmatically by using the **Add** method of the **Addons** collection.</span></span> 
    
<span data-ttu-id="6586b-127">Para obter mais informações sobre a execução de códigos no Visio, consulte [Sobre configurações de segurança e execução de códigos no Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) nesta Referência da ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6586b-127">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="6586b-p103">Em versões anteriores do Visio, essa função aparece como _RUNADDONWARGS. As versões 4.0 e posteriores do Visio aceitam os dois estilos.</span><span class="sxs-lookup"><span data-stu-id="6586b-p103">In earlier versions of Visio, this function appears as _RUNADDONWARGS. Visio application versions 4.0 and later accept either style.</span></span>
  
## <a name="example"></a><span data-ttu-id="6586b-130">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6586b-130">Example</span></span>

<span data-ttu-id="6586b-131">RUNADDONWARGS ("GRAPHMKR. EXE"," / GraphMaker = Stack ")</span><span class="sxs-lookup"><span data-stu-id="6586b-131">RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack")</span></span> 
  
<span data-ttu-id="6586b-132">Iniciará o complemento Graphmkr.exe e passará o argumento /GraphMaker=Stack.</span><span class="sxs-lookup"><span data-stu-id="6586b-132">Launches the add-on Graphmkr.exe and passes it the argument /GraphMaker=Stack.</span></span> 
  

