---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
localization_priority: Normal
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fdee0146ae2199097828e98abb96ffe43a64fc80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436626"
---
# <a name="xlfgetname"></a><span data-ttu-id="89f2b-104">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="89f2b-104">xlfGetName</span></span>

<span data-ttu-id="89f2b-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="89f2b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="89f2b-106">Retorna a definição de um nome como ele aparece na coluna **refere-se a** da caixa de diálogo **Gerenciador de nomes** , que é exibida quando você clica em **Gerenciador de nomes** na seção **nomes definidos** da guia **fórmulas** . Se a definição contiver referências, elas serão dadas como referências em estilo L1C1.</span><span class="sxs-lookup"><span data-stu-id="89f2b-106">Returns the definition of a name as it appears in the **Refers to** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. If the definition contains references, they are given as R1C1-style references.</span></span> <span data-ttu-id="89f2b-107">Use **xlfGetName** para verificar o valor definido por um nome.</span><span class="sxs-lookup"><span data-stu-id="89f2b-107">Use **xlfGetName** to check the value defined by a name.</span></span> <span data-ttu-id="89f2b-108">Para obter o nome que corresponde a uma definição, use [xlfGetDef](xlfgetdef.md).</span><span class="sxs-lookup"><span data-stu-id="89f2b-108">To get the name that corresponds to a definition, use [xlfGetDef](xlfgetdef.md).</span></span>
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a><span data-ttu-id="89f2b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89f2b-109">Parameters</span></span>

<span data-ttu-id="89f2b-110">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="89f2b-110">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="89f2b-111">Pode ser um nome definido na planilha; uma referência externa a um nome definido na pasta de trabalho ativa, por exemplo `"!Sales"`,; ou uma referência externa para um nome definido em uma determinada pasta de trabalho aberta, por `"[Book1]SHEET1!Sales"`exemplo,.</span><span class="sxs-lookup"><span data-stu-id="89f2b-111">Can be a name defined on the sheet; an external reference to a name defined on the active workbook, for example,  `"!Sales"`; or an external reference to a name defined on a particular open workbook, for example,  `"[Book1]SHEET1!Sales"`.</span></span>  <span data-ttu-id="89f2b-112">_pxNameText_ também pode ser um nome oculto.</span><span class="sxs-lookup"><span data-stu-id="89f2b-112">_pxNameText_ can also be a hidden name.</span></span> 
  
<span data-ttu-id="89f2b-113">_pxInfoType_ (**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="89f2b-113">_pxInfoType_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="89f2b-114">Especifica o tipo de informação a ser retornada sobre o nome.</span><span class="sxs-lookup"><span data-stu-id="89f2b-114">Specifies the type of information to return about the name.</span></span> <span data-ttu-id="89f2b-115">Se **false** ou omitido, a definição será retornada.</span><span class="sxs-lookup"><span data-stu-id="89f2b-115">If **FALSE** or omitted, the definition is returned.</span></span> <span data-ttu-id="89f2b-116">Se **true**, retornará **true** se o nome for definido para apenas a planilha, **false** se o nome for definido para a pasta de trabalho inteira.</span><span class="sxs-lookup"><span data-stu-id="89f2b-116">If **TRUE**, returns **TRUE** if the name is defined for just the sheet, **FALSE** if the name is defined for the entire workbook.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="89f2b-117">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="89f2b-117">Property value/Return value</span></span>

<span data-ttu-id="89f2b-118">_pxRes_ (**xltypeStr**, **xltypeBool**ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="89f2b-118">_pxRes_ (**xltypeStr**, **xltypeBool**, or **xltypeErr**)</span></span>
  
<span data-ttu-id="89f2b-119">Dependendo do valor passado por _pxInfoType_, retorna a definição do nome especificado (**XltypeStr**) ou **true** ou **false** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="89f2b-119">Depending on the value passed for  _pxInfoType_, returns the definition of the specified name (**xltypeStr**), or **TRUE** or **FALSE** (**xltypeBool**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="89f2b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="89f2b-120">Remarks</span></span>

<span data-ttu-id="89f2b-121">Se a caixa de seleção **proteger planilha e conteúdo de células bloqueadas** tiver sido selecionada na caixa de diálogo **proteger planilha** para proteger a pasta de trabalho que contém o `#N/A` nome, **xlfGetName** retornará o valor de erro.</span><span class="sxs-lookup"><span data-stu-id="89f2b-121">If the **Protect worksheet and contents of locked cells** check box has been selected in the **Protect Sheet** dialog box to protect the workbook containing the name, **xlfGetName** returns the  `#N/A` error value.</span></span> <span data-ttu-id="89f2b-122">Para ver a caixa de diálogo **proteger planilha** , clique em **proteger planilha** na seção **alterações** da guia **revisão** .</span><span class="sxs-lookup"><span data-stu-id="89f2b-122">To see the **Protect Sheet** dialog box, click **Protect Sheet** in the **Changes** section of the **Review** tab.</span></span> 
  
<span data-ttu-id="89f2b-123">A tabela a seguir lista três exemplos de valores retornados por uma chamada a **xlfGetDef** com o argumento _pxNameText_ especificado.</span><span class="sxs-lookup"><span data-stu-id="89f2b-123">The following table lists three examples of the values returned by a call to **xlfGetDef** with the specified  _pxNameText_ argument.</span></span> 
  
|<span data-ttu-id="89f2b-124">**Definição no Excel**</span><span class="sxs-lookup"><span data-stu-id="89f2b-124">**Definition in Excel**</span></span>|<span data-ttu-id="89f2b-125">**_pxNameText_**</span><span class="sxs-lookup"><span data-stu-id="89f2b-125">**_pxNameText_**</span></span>|<span data-ttu-id="89f2b-126">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="89f2b-126">**Value Returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="89f2b-127">O nome vendas em uma planilha é definido como o número 523.</span><span class="sxs-lookup"><span data-stu-id="89f2b-127">The name Sales on a sheet is defined as the number 523.</span></span>  <br/> |<span data-ttu-id="89f2b-128">Vendas</span><span class="sxs-lookup"><span data-stu-id="89f2b-128">"Sales"</span></span>  <br/> |<span data-ttu-id="89f2b-129">"= 523"</span><span class="sxs-lookup"><span data-stu-id="89f2b-129">"=523"</span></span>  <br/> |
|<span data-ttu-id="89f2b-130">O nome de lucro na planilha ativa é definido como a fórmula = vendas-custos.</span><span class="sxs-lookup"><span data-stu-id="89f2b-130">The name Profit on the active sheet is defined as the formula =Sales-Costs.</span></span>  <br/> |<span data-ttu-id="89f2b-131">"! Lucrativa</span><span class="sxs-lookup"><span data-stu-id="89f2b-131">"!Profit"</span></span>  <br/> |<span data-ttu-id="89f2b-132">"= Vendas-custos"</span><span class="sxs-lookup"><span data-stu-id="89f2b-132">"=Sales-Costs"</span></span>  <br/> |
|<span data-ttu-id="89f2b-133">O banco de dados de nomes na planilha ativa é definido como o intervalo a1: F500.</span><span class="sxs-lookup"><span data-stu-id="89f2b-133">The name Database on the active sheet is defined as the range A1:F500.</span></span>  <br/> |<span data-ttu-id="89f2b-134">"! AdventureWorks</span><span class="sxs-lookup"><span data-stu-id="89f2b-134">"!Database"</span></span>  <br/> |<span data-ttu-id="89f2b-135">"= L1C1: R500C6"</span><span class="sxs-lookup"><span data-stu-id="89f2b-135">"=R1C1:R500C6"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89f2b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="89f2b-136">See also</span></span>

- [<span data-ttu-id="89f2b-137">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="89f2b-137">xlfGetDef</span></span>](xlfgetdef.md)
- [<span data-ttu-id="89f2b-138">Funções XLM essenciais e úteis para a API C</span><span class="sxs-lookup"><span data-stu-id="89f2b-138">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

