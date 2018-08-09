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
ms.openlocfilehash: 63bfc6e94950a621c2367b2d35d25e3de48b344f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765463"
---
# <a name="xlfgetname"></a><span data-ttu-id="4eb1b-104">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="4eb1b-104">xlfGetName</span></span>

<span data-ttu-id="4eb1b-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4eb1b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4eb1b-106">Retorna a definição de um nome como ele aparece na coluna da caixa de diálogo **Gerenciador de nome** , que é exibida quando você clicar em **Nome do gerente** , na seção **Nomes definidos** na guia **fórmulas** **refere-se a** . Se a definição contém referências, ele recebe como referências em estilo L1C1.</span><span class="sxs-lookup"><span data-stu-id="4eb1b-106">Returns the definition of a name as it appears in the **Refers to** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. If the definition contains references, they are given as R1C1-style references.</span></span> <span data-ttu-id="4eb1b-107">Use **xlfGetName** para verificar o valor definido por um nome.</span><span class="sxs-lookup"><span data-stu-id="4eb1b-107">Use **xlfGetName** to check the value defined by a name.</span></span> <span data-ttu-id="4eb1b-108">Para obter o nome que corresponde a uma definição, use [xlfGetDef](xlfgetdef.md).</span><span class="sxs-lookup"><span data-stu-id="4eb1b-108">To get the name that corresponds to a definition, use [xlfGetDef](xlfgetdef.md).</span></span>
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a><span data-ttu-id="4eb1b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4eb1b-109">Parameters</span></span>

<span data-ttu-id="4eb1b-110">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="4eb1b-110">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="4eb1b-111">Pode ser um nome definido na planilha; uma referência externa para um nome definido na planilha ativa, por exemplo, `"!Sales"`; ou uma referência externa para um nome definido em uma determinada pasta de trabalho aberta, por exemplo, `"[Book1]SHEET1!Sales"`.</span><span class="sxs-lookup"><span data-stu-id="4eb1b-111">Can be a name defined on the sheet; an external reference to a name defined on the active workbook, for example,  `"!Sales"`; or an external reference to a name defined on a particular open workbook, for example,  `"[Book1]SHEET1!Sales"`.</span></span>  <span data-ttu-id="4eb1b-112">_pxNameText_ também pode ser um nome oculto.</span><span class="sxs-lookup"><span data-stu-id="4eb1b-112">_pxNameText_ can also be a hidden name.</span></span> 
  
<span data-ttu-id="4eb1b-113">_pxInfoType_ (**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="4eb1b-113">_pxInfoType_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="4eb1b-114">Especifica o tipo de informações que serão retornadas sobre o nome.</span><span class="sxs-lookup"><span data-stu-id="4eb1b-114">Specifies the type of information to return about the name.</span></span> <span data-ttu-id="4eb1b-115">Se **Falso** ou omitido, a definição é retornada.</span><span class="sxs-lookup"><span data-stu-id="4eb1b-115">If **FALSE** or omitted, the definition is returned.</span></span> <span data-ttu-id="4eb1b-116">Se **TRUE**, retorna **TRUE** se o nome está definido apenas da planilha, **FALSE** se o nome está definido para a pasta de trabalho inteira.</span><span class="sxs-lookup"><span data-stu-id="4eb1b-116">If **TRUE**, returns **TRUE** if the name is defined for just the sheet, **FALSE** if the name is defined for the entire workbook.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="4eb1b-117">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4eb1b-117">Property value/Return value</span></span>

<span data-ttu-id="4eb1b-118">_pxRes_ (**xltypeStr**, **xltypeBool**ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="4eb1b-118">_pxRes_ (**xltypeStr**, **xltypeBool**, or **xltypeErr**)</span></span>
  
<span data-ttu-id="4eb1b-119">Dependendo do valor passado para _pxInfoType_, retorna a definição do nome especificado (**xltypeStr**) ou **TRUE** ou **FALSE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="4eb1b-119">Depending on the value passed for  _pxInfoType_, returns the definition of the specified name (**xltypeStr**), or **TRUE** or **FALSE** (**xltypeBool**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4eb1b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4eb1b-120">Remarks</span></span>

<span data-ttu-id="4eb1b-121">Se a caixa de seleção de **proteger a planilha e o conteúdo de células bloqueadas** tiver sido selecionada na caixa de diálogo **Proteger planilha** para proteger a pasta de trabalho que contém o nome, **xlfGetName** retorna o `#N/A` o valor de erro.</span><span class="sxs-lookup"><span data-stu-id="4eb1b-121">If the **Protect worksheet and contents of locked cells** check box has been selected in the **Protect Sheet** dialog box to protect the workbook containing the name, **xlfGetName** returns the  `#N/A` error value.</span></span> <span data-ttu-id="4eb1b-122">Para ver a caixa de diálogo **Proteger planilha** , clique em **Proteger planilha** na seção **alterações** da guia **revisão** .</span><span class="sxs-lookup"><span data-stu-id="4eb1b-122">To see the **Protect Sheet** dialog box, click **Protect Sheet** in the **Changes** section of the **Review** tab.</span></span> 
  
<span data-ttu-id="4eb1b-123">A tabela a seguir lista os três exemplos dos valores retornados por uma chamada para **xlfGetDef** com o argumento especificado _pxNameText_ .</span><span class="sxs-lookup"><span data-stu-id="4eb1b-123">The following table lists three examples of the values returned by a call to **xlfGetDef** with the specified  _pxNameText_ argument.</span></span> 
  
|<span data-ttu-id="4eb1b-124">**Definição no Excel**</span><span class="sxs-lookup"><span data-stu-id="4eb1b-124">**Definition in Excel**</span></span>|<span data-ttu-id="4eb1b-125">**_pxNameText_**</span><span class="sxs-lookup"><span data-stu-id="4eb1b-125">**_pxNameText_**</span></span>|<span data-ttu-id="4eb1b-126">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="4eb1b-126">**Value Returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4eb1b-127">O nome de vendas em uma planilha é definido como o número 523.</span><span class="sxs-lookup"><span data-stu-id="4eb1b-127">The name Sales on a sheet is defined as the number 523.</span></span>  <br/> |<span data-ttu-id="4eb1b-128">"Vendas"</span><span class="sxs-lookup"><span data-stu-id="4eb1b-128">"Sales"</span></span>  <br/> |<span data-ttu-id="4eb1b-129">"= 523"</span><span class="sxs-lookup"><span data-stu-id="4eb1b-129">"=523"</span></span>  <br/> |
|<span data-ttu-id="4eb1b-130">O nome de lucro na planilha ativa é definido como a fórmula = custos de vendas.</span><span class="sxs-lookup"><span data-stu-id="4eb1b-130">The name Profit on the active sheet is defined as the formula =Sales-Costs.</span></span>  <br/> |<span data-ttu-id="4eb1b-131">"! Lucro"</span><span class="sxs-lookup"><span data-stu-id="4eb1b-131">"!Profit"</span></span>  <br/> |<span data-ttu-id="4eb1b-132">"= Custos de vendas"</span><span class="sxs-lookup"><span data-stu-id="4eb1b-132">"=Sales-Costs"</span></span>  <br/> |
|<span data-ttu-id="4eb1b-133">O nome do banco de dados na planilha ativa é definido como o intervalo A1:F500.</span><span class="sxs-lookup"><span data-stu-id="4eb1b-133">The name Database on the active sheet is defined as the range A1:F500.</span></span>  <br/> |<span data-ttu-id="4eb1b-134">"! Banco de dados"</span><span class="sxs-lookup"><span data-stu-id="4eb1b-134">"!Database"</span></span>  <br/> |<span data-ttu-id="4eb1b-135">"= R1C1:R500C6"</span><span class="sxs-lookup"><span data-stu-id="4eb1b-135">"=R1C1:R500C6"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4eb1b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="4eb1b-136">See also</span></span>

- [<span data-ttu-id="4eb1b-137">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="4eb1b-137">xlfGetDef</span></span>](xlfgetdef.md)
- [<span data-ttu-id="4eb1b-138">Funções XLM essenciais e úteis para a API de C</span><span class="sxs-lookup"><span data-stu-id="4eb1b-138">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

