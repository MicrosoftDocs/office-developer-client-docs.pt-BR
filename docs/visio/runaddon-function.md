---
title: Função RUNADDON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251492
localization_priority: Normal
ms.assetid: 122c1d30-3cb9-7e7d-b4cc-e93ab8e4da4f
description: Executa um complemento ou uma macro em um projeto do Microsoft Visual Basic for Applications (VBA).
ms.openlocfilehash: 280f6eaf1e5db045d8c1d22965df00960d188112
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319058"
---
# <a name="runaddon-function"></a><span data-ttu-id="812fa-103">Função RUNADDON</span><span class="sxs-lookup"><span data-stu-id="812fa-103">RUNADDON Function</span></span>

<span data-ttu-id="812fa-104">Executa um complemento ou uma macro em um projeto do Microsoft Visual Basic for Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="812fa-104">Executes an add-on or a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="812fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="812fa-105">Syntax</span></span>

<span data-ttu-id="812fa-106">RUNADDON (" *cadeia de caracteres* ")</span><span class="sxs-lookup"><span data-stu-id="812fa-106">RUNADDON(" *string*  ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="812fa-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="812fa-107">Parameters</span></span>

|<span data-ttu-id="812fa-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="812fa-108">**Name**</span></span>|<span data-ttu-id="812fa-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="812fa-109">**Required/Optional**</span></span>|<span data-ttu-id="812fa-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="812fa-110">**Data Type**</span></span>|<span data-ttu-id="812fa-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="812fa-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="812fa-112">_string_</span><span class="sxs-lookup"><span data-stu-id="812fa-112">_string_</span></span> <br/> |<span data-ttu-id="812fa-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="812fa-113">Required</span></span>  <br/> |<span data-ttu-id="812fa-114">**String**</span><span class="sxs-lookup"><span data-stu-id="812fa-114">**String**</span></span> <br/> | <span data-ttu-id="812fa-115">O nome de um complemento na coleção **Addons** ou de uma macro em um projeto VBA.</span><span class="sxs-lookup"><span data-stu-id="812fa-115">The name of an add-on in the **Addons** collection or a macro in a VBA project.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="812fa-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="812fa-116">Remarks</span></span>

<span data-ttu-id="812fa-117">Se o projeto do documento que contém a chamada de função RUNADDON (ou outro projeto se for referenciado) não tiver uma macro (um procedimento sem argumentos) chamado _String_, o Microsoft Visio executará o complemento chamado _String_.</span><span class="sxs-lookup"><span data-stu-id="812fa-117">If the project of the document that contains the RUNADDON function call (or another project if it is referenced) does not have a macro (a procedure with no arguments) named  _string_, Microsoft Visio runs the add-on named  _string_.</span></span> <span data-ttu-id="812fa-118">Se nenhuma _cadeia de caracteres_ nomeada de complemento puder ser encontrada, o Visio não fará nada e não informará nenhum erro.</span><span class="sxs-lookup"><span data-stu-id="812fa-118">If no add-on named  _string_ can be found, Visio does nothing and reports no error.</span></span> <span data-ttu-id="812fa-119">(Você pode usar a propriedade **TraceFlags** para monitorar os procedimentos e complementos que o Visio tenta executar.)</span><span class="sxs-lookup"><span data-stu-id="812fa-119">(You can use the **TraceFlags** property to monitor the procedures and add-ons that Visio attempts to run.)</span></span> 
  
<span data-ttu-id="812fa-120">Ao chamar um procedimento em um módulo padrão, é recomendável prefixar a cadeia de caracteres com o nome do módulo que contém o procedimento (por exemplo, *ModuleName. ProcName*), porque mais de um módulo pode ter um procedimento com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="812fa-120">When you call a procedure in a standard module, it is recommended that you prefix the string with the module name that contains the procedure (for example,  *moduleName.procName*), because more than one module can have a procedure with the same name.</span></span> 
  
<span data-ttu-id="812fa-121">Para chamar um procedimento em um projeto diferente do projeto do documento que contém a chamada de função RUNADDON, use a sintaxe *ProjName. modName. ProcName* (você deve ter definido explicitamente uma referência ao *ProjName* no projeto VBA).</span><span class="sxs-lookup"><span data-stu-id="812fa-121">To call a procedure in a project other than the project of the document that contains the RUNADDON function call, use the syntax  *projName.modName.procName*  (you must have explicitly set a reference to  *projName*  in your VBA project).</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="812fa-p102">Iniciando com o Visio 2002, a função RUNADDON não pode executar uma sequência de caracteres contendo código VBA arbitrário. Códigos que tenham anteriormente passado para a função RUNADDON podem ser movidos para um procedimento no projeto VBA de um documento que é chamado a partir da função RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="812fa-p102">Beginning with Visio 2002, the RUNADDON function cannot execute a string containing arbitrary VBA code. Code that was formerly passed to the RUNADDON function can be moved to a procedure in a document's VBA project that is called from the RUNADDON function.</span></span> 
  
<span data-ttu-id="812fa-124">Para obter mais informações sobre a execução de códigos no Visio, consulte [Sobre configurações de segurança e execução de códigos no Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) nesta Referência da ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="812fa-124">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="812fa-p103">Em versões anteriores do Visio, essa função aparece como _RUNADDON. As versões 4.0 e posteriores do Visio aceitam os dois estilos.</span><span class="sxs-lookup"><span data-stu-id="812fa-p103">In earlier versions of Visio, this function appears as _RUNADDON. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="812fa-127">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="812fa-127">Example 1</span></span>

<span data-ttu-id="812fa-128">RUNADDON ("Calendar. exe")</span><span class="sxs-lookup"><span data-stu-id="812fa-128">RUNADDON("Calendar.exe")</span></span>
  
<span data-ttu-id="812fa-129">Inicia um complemento chamado Calendar. exe.</span><span class="sxs-lookup"><span data-stu-id="812fa-129">Launches an add-on called Calendar.exe.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="812fa-130">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="812fa-130">Example 2</span></span>

<span data-ttu-id="812fa-131">RUNADDON("Arranjar Formas")</span><span class="sxs-lookup"><span data-stu-id="812fa-131">RUNADDON("Array Shapes")</span></span>
  
<span data-ttu-id="812fa-132">Inicia o complemento (implementado em VSL) cujo nome é Arranjar formas.</span><span class="sxs-lookup"><span data-stu-id="812fa-132">Launches the (VSL-implemented) add-on whose name is Array Shapes.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="812fa-133">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="812fa-133">Example 3</span></span>

<span data-ttu-id="812fa-134">RUNADDON ("ThisDocument. ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="812fa-134">RUNADDON("ThisDocument.ReportStatistics")</span></span>
  
<span data-ttu-id="812fa-135">Chama a macro ReportStatistics no módulo **EsteDocumento** no projeto do documento contendo essa chamada de função.</span><span class="sxs-lookup"><span data-stu-id="812fa-135">Calls the ReportStatistics macro in the **ThisDocument** module in the document project containing this function call.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="812fa-136">Para invocar a macro no módulo **ThisDocument**, anteceda a cadeia de caracteres com "EsteDocumento" como mostrado.</span><span class="sxs-lookup"><span data-stu-id="812fa-136">To invoke a macro in the **ThisDocument** module, you must preface the string with "ThisDocument" as shown.</span></span> 
  
## <a name="example-4"></a><span data-ttu-id="812fa-137">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="812fa-137">Example 4</span></span>

<span data-ttu-id="812fa-138">RUNADDON (" *ModuleName* . ReportStatistics ")</span><span class="sxs-lookup"><span data-stu-id="812fa-138">RUNADDON(" *ModuleName*  .ReportStatistics")</span></span> 
  
<span data-ttu-id="812fa-139">Chama a macro ReportStatistics em *ModuleName* no projeto de documento que contém essa chamada de função.</span><span class="sxs-lookup"><span data-stu-id="812fa-139">Calls the ReportStatistics macro in  *ModuleName*  in the document project that contains this function call.</span></span> 
  

