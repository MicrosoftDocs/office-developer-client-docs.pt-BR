---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 030c4e501e8a9eb4b6ce29d7fe0e171324b50b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765484"
---
# <a name="xlfgetdef"></a><span data-ttu-id="ed18e-104">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="ed18e-104">xlfGetDef</span></span>

<span data-ttu-id="ed18e-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ed18e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ed18e-106">Retorna o nome, como texto, que é definido para uma determinada área, valor ou fórmula em uma pasta de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ed18e-106">Returns the name, as text, that is defined for a particular area, value, or formula in a workbook.</span></span> <span data-ttu-id="ed18e-107">No Excel, esse valor é exibido na coluna **nome** da caixa de diálogo **Gerenciador de nome** , que é exibida quando você clicar em **Nome do gerente** na seção **Nomes definidos** , na guia **fórmulas** de uso **xlfGetDef** para obter o nome que corresponde a uma definição.</span><span class="sxs-lookup"><span data-stu-id="ed18e-107">In Excel, this value is displayed in the **Name** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. Use **xlfGetDef** to get the name that corresponds to a definition.</span></span> <span data-ttu-id="ed18e-108">Para obter a definição de um nome, use [xlfGetName](xlfgetname.md).</span><span class="sxs-lookup"><span data-stu-id="ed18e-108">To get the definition of a name, use [xlfGetName](xlfgetname.md).</span></span>
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a><span data-ttu-id="ed18e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed18e-109">Parameters</span></span>

<span data-ttu-id="ed18e-110">_pxDefText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="ed18e-110">_pxDefText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="ed18e-111">Pode ser a qualquer coisa que você pode definir um nome para se referir a, incluindo uma referência, um valor, um objeto ou uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="ed18e-111">Can be anything you can define a name to refer to, including a reference, a value, an object, or a formula.</span></span>
  
<span data-ttu-id="ed18e-112">Referências devem ser fornecidas em estilo L1C1, tais como `"R3C5"`.</span><span class="sxs-lookup"><span data-stu-id="ed18e-112">References must be given in R1C1 style, such as  `"R3C5"`.</span></span> <span data-ttu-id="ed18e-113">Se _pxDefText_ for um valor ou fórmula, não é necessário incluir o sinal de igualdade que é exibido na coluna **Refere-se a** na caixa de diálogo **Gerenciador de nome** .</span><span class="sxs-lookup"><span data-stu-id="ed18e-113">If  _pxDefText_ is a value or formula, it is not necessary to include the equal sign that is displayed in the **Refers To** column in the **Name Manager** dialog box.</span></span> <span data-ttu-id="ed18e-114">Se houver mais de um nome para _pxDefText_, **xlfGetDef** retorna o primeiro nome.</span><span class="sxs-lookup"><span data-stu-id="ed18e-114">If there is more than one name for  _pxDefText_, **xlfGetDef** returns the first name.</span></span> <span data-ttu-id="ed18e-115">Se nenhum nome corresponde _pxDefText_, **xlfGetDef** retorna o `#NAME?` o valor de erro.</span><span class="sxs-lookup"><span data-stu-id="ed18e-115">If no name matches  _pxDefText_, **xlfGetDef** returns the  `#NAME?` error value.</span></span> 
  
<span data-ttu-id="ed18e-116">_pxDocumentText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="ed18e-116">_pxDocumentText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="ed18e-117">Especifica a planilha que _pxDefText_ está em.</span><span class="sxs-lookup"><span data-stu-id="ed18e-117">Specifies the sheet that  _pxDefText_ is on.</span></span> <span data-ttu-id="ed18e-118">Se _pxDocumentText_ for omitido, presume-se para ser da planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="ed18e-118">If  _pxDocumentText_ is omitted, it is assumed to be the active sheet.</span></span> 
  
<span data-ttu-id="ed18e-119">_pxTypeNum_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="ed18e-119">_pxTypeNum_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="ed18e-120">Um número de 1 a 3 para especificar quais tipos de nomes são retornados.</span><span class="sxs-lookup"><span data-stu-id="ed18e-120">A number from 1 to 3 specifying which types of names are returned.</span></span>
  
|<span data-ttu-id="ed18e-121">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="ed18e-121">**_pxTypeNum_**</span></span>|<span data-ttu-id="ed18e-122">**Retorna**</span><span class="sxs-lookup"><span data-stu-id="ed18e-122">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ed18e-123">1 ou omitido</span><span class="sxs-lookup"><span data-stu-id="ed18e-123">1 or omitted</span></span>  <br/> |<span data-ttu-id="ed18e-124">Apenas nomes normais.</span><span class="sxs-lookup"><span data-stu-id="ed18e-124">Normal names only.</span></span>  <br/> |
|<span data-ttu-id="ed18e-125">2</span><span class="sxs-lookup"><span data-stu-id="ed18e-125">2</span></span>  <br/> |<span data-ttu-id="ed18e-126">Apenas nomes ocultos.</span><span class="sxs-lookup"><span data-stu-id="ed18e-126">Hidden names only.</span></span>  <br/> |
|<span data-ttu-id="ed18e-127">3</span><span class="sxs-lookup"><span data-stu-id="ed18e-127">3</span></span>  <br/> |<span data-ttu-id="ed18e-128">Todos os nomes.</span><span class="sxs-lookup"><span data-stu-id="ed18e-128">All names.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="ed18e-129">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed18e-129">Property value/Return value</span></span>

 <span data-ttu-id="ed18e-130">_pxRes_ (**xltypeStr** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="ed18e-130">_pxRes_ (**xltypeStr** or **xltypeErr**)</span></span>
  
<span data-ttu-id="ed18e-131">Retorna o nome associado à definição especificada.</span><span class="sxs-lookup"><span data-stu-id="ed18e-131">Returns the name associated with the specified definition.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed18e-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed18e-132">Remarks</span></span>

<span data-ttu-id="ed18e-133">A tabela a seguir lista os quatro exemplos dos valores retornados por uma chamada para **xlfGetDef** com os argumentos especificados.</span><span class="sxs-lookup"><span data-stu-id="ed18e-133">The following table lists four examples of the values returned by a call to **xlfGetDef** with the specified arguments.</span></span> 
  
|<span data-ttu-id="ed18e-134">**Nome definido no Excel**</span><span class="sxs-lookup"><span data-stu-id="ed18e-134">**Name defined in Excel**</span></span>|<span data-ttu-id="ed18e-135">**_pxDefText_**</span><span class="sxs-lookup"><span data-stu-id="ed18e-135">**_pxDefText_**</span></span>|<span data-ttu-id="ed18e-136">**_pxDocumentText_**</span><span class="sxs-lookup"><span data-stu-id="ed18e-136">**_pxDocumentText_**</span></span>|<span data-ttu-id="ed18e-137">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="ed18e-137">**_pxTypeNum_**</span></span>|<span data-ttu-id="ed18e-138">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="ed18e-138">**Value Returned**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ed18e-139">O intervalo especificado em Sheet4 é chamado Sales.</span><span class="sxs-lookup"><span data-stu-id="ed18e-139">The specified range in Sheet4 is named Sales.</span></span>  <br/> |<span data-ttu-id="ed18e-140">"R2C2:R9C6"</span><span class="sxs-lookup"><span data-stu-id="ed18e-140">"R2C2:R9C6"</span></span>  <br/> |<span data-ttu-id="ed18e-141">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="ed18e-141">"Sheet4"</span></span>  <br/> |<span data-ttu-id="ed18e-142">\<omitido\></span><span class="sxs-lookup"><span data-stu-id="ed18e-142">\<omitted\></span></span>  <br/> |<span data-ttu-id="ed18e-143">"Vendas"</span><span class="sxs-lookup"><span data-stu-id="ed18e-143">"Sales"</span></span>  <br/> |
|<span data-ttu-id="ed18e-144">O valor de 100 em Sheet4 é definido como constante.</span><span class="sxs-lookup"><span data-stu-id="ed18e-144">The value 100 in Sheet4 is defined as Constant.</span></span>  <br/> |<span data-ttu-id="ed18e-145">"100"</span><span class="sxs-lookup"><span data-stu-id="ed18e-145">"100"</span></span>  <br/> |<span data-ttu-id="ed18e-146">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="ed18e-146">"Sheet4"</span></span>  <br/> |<span data-ttu-id="ed18e-147">\<omitido\></span><span class="sxs-lookup"><span data-stu-id="ed18e-147">\<omitted\></span></span>  <br/> |<span data-ttu-id="ed18e-148">"Constante"</span><span class="sxs-lookup"><span data-stu-id="ed18e-148">"Constant"</span></span>  <br/> |
|<span data-ttu-id="ed18e-149">A fórmula especificada no Sheet4 é nomeada SumTotal.</span><span class="sxs-lookup"><span data-stu-id="ed18e-149">The specified formula in Sheet4 is named SumTotal.</span></span>  <br/> |<span data-ttu-id="ed18e-150">"SUM(R1C1:R10C1)"</span><span class="sxs-lookup"><span data-stu-id="ed18e-150">"SUM(R1C1:R10C1)"</span></span>  <br/> |<span data-ttu-id="ed18e-151">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="ed18e-151">"Sheet4"</span></span>  <br/> |<span data-ttu-id="ed18e-152">\<omitido\></span><span class="sxs-lookup"><span data-stu-id="ed18e-152">\<omitted\></span></span>  <br/> |<span data-ttu-id="ed18e-153">"SumTotal"</span><span class="sxs-lookup"><span data-stu-id="ed18e-153">"SumTotal"</span></span>  <br/> |
|<span data-ttu-id="ed18e-154">3 é definido como o contador de nome oculto na planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="ed18e-154">3 is defined as the hidden name Counter on the active sheet.</span></span>  <br/> |<span data-ttu-id="ed18e-155">"3"</span><span class="sxs-lookup"><span data-stu-id="ed18e-155">"3"</span></span>  <br/> |<span data-ttu-id="ed18e-156">\<omitido\></span><span class="sxs-lookup"><span data-stu-id="ed18e-156">\<omitted\></span></span>  <br/> |<span data-ttu-id="ed18e-157">2</span><span class="sxs-lookup"><span data-stu-id="ed18e-157">2</span></span>  <br/> |<span data-ttu-id="ed18e-158">"Contador"</span><span class="sxs-lookup"><span data-stu-id="ed18e-158">"Counter"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed18e-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed18e-159">See also</span></span>

- [<span data-ttu-id="ed18e-160">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="ed18e-160">xlfGetName</span></span>](xlfgetname.md)
- [<span data-ttu-id="ed18e-161">Funções XLM essenciais e úteis para a API de C</span><span class="sxs-lookup"><span data-stu-id="ed18e-161">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

