---
title: Função RUNMACRO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033809
localization_priority: Normal
ms.assetid: 86b0f071-5e0b-56de-ff5b-63c114ad823a
description: Chama uma macro em um Microsoft Visual Basic para o project Applications (VBA).
ms.openlocfilehash: e3dd989956ce9c5f795ae3ef0d8535ab2776d6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772832"
---
# <a name="runmacro-function"></a><span data-ttu-id="15d16-103">Função RUNMACRO</span><span class="sxs-lookup"><span data-stu-id="15d16-103">RUNMACRO Function</span></span>

<span data-ttu-id="15d16-104">Chama uma macro em um Microsoft Visual Basic para o project Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="15d16-104">Calls a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="15d16-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15d16-105">Syntax</span></span>

<span data-ttu-id="15d16-106">RUNMACRO (* * *macroname* * * [, * * *nomeProj_opc* * *])</span><span class="sxs-lookup"><span data-stu-id="15d16-106">RUNMACRO (** *macroname* ** [, ** *projname_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="15d16-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15d16-107">Parameters</span></span>

|<span data-ttu-id="15d16-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="15d16-108">**Name**</span></span>|<span data-ttu-id="15d16-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="15d16-109">**Required/Optional**</span></span>|<span data-ttu-id="15d16-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="15d16-110">**Data Type**</span></span>|<span data-ttu-id="15d16-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="15d16-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="15d16-112">_macroname_</span><span class="sxs-lookup"><span data-stu-id="15d16-112">_macroname_</span></span> <br/> |<span data-ttu-id="15d16-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="15d16-113">Required</span></span>  <br/> |<span data-ttu-id="15d16-114">**String**</span><span class="sxs-lookup"><span data-stu-id="15d16-114">**String**</span></span> <br/> |<span data-ttu-id="15d16-115">O nome da macro a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="15d16-115">The name of the macro to call.</span></span>  <br/> |
| <span data-ttu-id="15d16-116">_nomeProj_opc_</span><span class="sxs-lookup"><span data-stu-id="15d16-116">_projname_opt_</span></span> <br/> |<span data-ttu-id="15d16-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="15d16-117">Optional</span></span>  <br/> |<span data-ttu-id="15d16-118">**String**</span><span class="sxs-lookup"><span data-stu-id="15d16-118">**String**</span></span> <br/> | <span data-ttu-id="15d16-119">O projeto que contém a macro.</span><span class="sxs-lookup"><span data-stu-id="15d16-119">The project that contains the macro.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15d16-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="15d16-120">Remarks</span></span>

<span data-ttu-id="15d16-121">Se um projeto for especificado, o Microsoft Visio verifica todos os documentos abertos para a um que contêm chamadas e _nomeProj_opc_ _macroname_ no projeto.</span><span class="sxs-lookup"><span data-stu-id="15d16-121">If a project is specified, Microsoft Visio scans all open documents for the one containing  _projname_opt_ and calls  _macroname_ in that project.</span></span> <span data-ttu-id="15d16-122">Se _nomeProj_opc_ for omitido ou nulo (""), _macroname_ será considerado no projeto VBA do documento que contém a fórmula RUNMACRO sendo avaliada.</span><span class="sxs-lookup"><span data-stu-id="15d16-122">If  _projname_opt_ is omitted or null (""),  _macroname_ is assumed to be in the VBA project of the document that contains the RUNMACRO formula being evaluated.</span></span> 
  
<span data-ttu-id="15d16-123">A função RUNMACRO difere da função CALLTHIS não passe uma referência para a forma que contém a fórmula sendo avaliada para _macroname_.</span><span class="sxs-lookup"><span data-stu-id="15d16-123">The RUNMACRO function differs from the CALLTHIS function in that it does not pass a reference to the shape that owns the formula being evaluated to  _macroname_.</span></span> <span data-ttu-id="15d16-124">Assim como CALLTHIS, a função RUNMACRO não exige uma referência para _nomeProj_opc_ para ligar para ele.</span><span class="sxs-lookup"><span data-stu-id="15d16-124">Like CALLTHIS, the RUNMACRO function doesn't require a reference to  _projname_opt_ to call into it.</span></span> 
  
 <span data-ttu-id="15d16-125">O código VBA, que é invocado quando a instância do Visio avalia uma função RUNMACRO em uma fórmula, não deve fechar o documento que contém a célula que está usando a função, uma vez que ocorrerá um erro de aplicativo e o Visio será fechado.</span><span class="sxs-lookup"><span data-stu-id="15d16-125">VBA code that is invoked when the Visio instance evaluates a RUNMACRO function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="15d16-126">Se você precisar fechar o documento que contém a célula que está utilizando a função RUNMACRO, utilize uma das técnicas a seguir:</span><span class="sxs-lookup"><span data-stu-id="15d16-126">If you need to close the document containing the cell that uses the RUNMACRO function, use one of the following techniques:</span></span>
  
- <span data-ttu-id="15d16-127">Feche o documento a partir de um código que não seja VBA.</span><span class="sxs-lookup"><span data-stu-id="15d16-127">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="15d16-128">Feche o documento a partir de um projeto diferente do que está sendo fechado.</span><span class="sxs-lookup"><span data-stu-id="15d16-128">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="15d16-129">Envie mensagens de janela para fechar as janelas em vez de fechar o documento.</span><span class="sxs-lookup"><span data-stu-id="15d16-129">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="15d16-130">Para obter mais informações sobre a execução de códigos no Visio, consulte [Sobre configurações de segurança e execução de códigos no Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) nesta Referência da ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="15d16-130">For more information about running code in Visio, see [About security settings and running code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="15d16-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="15d16-131">Example</span></span>

<span data-ttu-id="15d16-132">O exemplo a seguir invoca uma macro chamada MeuTeste no modelo de classe EsteDocumento do projeto VBA que contém a fórmula RUNMACRO.</span><span class="sxs-lookup"><span data-stu-id="15d16-132">The following example invokes a macro called MyTest in the ThisDocument class module of the VBA project containing the RUNMACRO formula.</span></span> 
  
<span data-ttu-id="15d16-133">RUNMACRO ("EsteDocumento.MeuTeste")</span><span class="sxs-lookup"><span data-stu-id="15d16-133">RUNMACRO ("ThisDocument.MyTest")</span></span> 
  

