---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- função xlSet [Excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0912c1d40882933778d0df927ceb9de773063444
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303854"
---
# <a name="xlset"></a><span data-ttu-id="2eac5-104">xlSet</span><span class="sxs-lookup"><span data-stu-id="2eac5-104">xlSet</span></span>

<span data-ttu-id="2eac5-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2eac5-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2eac5-106">Coloca valores constantes em células ou intervalos muito rapidamente.</span><span class="sxs-lookup"><span data-stu-id="2eac5-106">Puts constant values into cells or ranges very quickly.</span></span> <span data-ttu-id="2eac5-107">Para obter mais informações, consulte "xlSet e pastas de trabalho com fórmulas de matriz" em [problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="2eac5-107">For more information, see "xlSet and Workbooks with Array Formulas" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a><span data-ttu-id="2eac5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eac5-108">Parameters</span></span>

<span data-ttu-id="2eac5-109">_pxReference_ (**xltypeRef** ou **xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="2eac5-109">_pxReference_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="2eac5-110">Uma referência retangular que descreve a célula ou células de destino.</span><span class="sxs-lookup"><span data-stu-id="2eac5-110">A rectangular reference describing the target cell or cells.</span></span> <span data-ttu-id="2eac5-111">A referência deve descrever as células adjacentes, de forma que em um **xltypeRef** `val.mref.lpmref->count` deve ser definido como 1.</span><span class="sxs-lookup"><span data-stu-id="2eac5-111">The reference must describe adjacent cells, so that in an **xltypeRef** `val.mref.lpmref->count` must be set to 1.</span></span> 
  
<span data-ttu-id="2eac5-112">_pxValue_</span><span class="sxs-lookup"><span data-stu-id="2eac5-112">_pxValue_</span></span>
  
<span data-ttu-id="2eac5-113">O valor ou valores a serem colocados na célula ou nas células.</span><span class="sxs-lookup"><span data-stu-id="2eac5-113">The value or values to be placed into the cell or cells.</span></span> <span data-ttu-id="2eac5-114">Para obter mais informações, consulte a seção "Comentários".</span><span class="sxs-lookup"><span data-stu-id="2eac5-114">For more information, see the "Remarks" section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2eac5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2eac5-115">Remarks</span></span>

### <a name="pxvalue-argument"></a><span data-ttu-id="2eac5-116">argumento pxValue</span><span class="sxs-lookup"><span data-stu-id="2eac5-116">pxValue argument</span></span>

<span data-ttu-id="2eac5-117">_pxValue_ pode ser um valor ou uma matriz.</span><span class="sxs-lookup"><span data-stu-id="2eac5-117">_pxValue_ can either be a value or an array.</span></span> <span data-ttu-id="2eac5-118">Se for um valor, todo o intervalo de destino será preenchido com esse valor.</span><span class="sxs-lookup"><span data-stu-id="2eac5-118">If it is a value, the entire destination range is filled with that value.</span></span> <span data-ttu-id="2eac5-119">Se for uma matriz (**xltypeMulti**), os elementos da matriz são colocados nos locais correspondentes no retângulo.</span><span class="sxs-lookup"><span data-stu-id="2eac5-119">If it is an array (**xltypeMulti**), the elements of the array are put into the corresponding locations in the rectangle.</span></span>
  
<span data-ttu-id="2eac5-120">Se você usar uma matriz horizontal para o segundo argumento, ela será duplicada para baixo para preencher todo o retângulo.</span><span class="sxs-lookup"><span data-stu-id="2eac5-120">If you use a horizontal array for the second argument, it is duplicated down to fill the entire rectangle.</span></span> <span data-ttu-id="2eac5-121">Se você usar uma matriz vertical, ela será duplicada à direita para preencher o retângulo inteiro.</span><span class="sxs-lookup"><span data-stu-id="2eac5-121">If you use a vertical array, it is duplicated right to fill the entire rectangle.</span></span> <span data-ttu-id="2eac5-122">Se você usar uma matriz retangular e for muito pequena para o intervalo retangular em que você deseja colocá-la, esse intervalo será preenchido com **#N/a**s.</span><span class="sxs-lookup"><span data-stu-id="2eac5-122">If you use a rectangular array, and it is too small for the rectangular range you want to put it in, that range is padded with **#N/A**s.</span></span>
  
<span data-ttu-id="2eac5-123">Se o intervalo de destino for menor do que a matriz de origem, os valores serão copiados até os limites do intervalo de destino e os dados adicionais serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="2eac5-123">If the target range is smaller than the source array, the values are copied in up to the limits of the target range and the extra data are ignored.</span></span>
  
<span data-ttu-id="2eac5-124">Para limpar um elemento do retângulo de destino, use um elemento de matriz de tipo **xltypeNil** na matriz de origem.</span><span class="sxs-lookup"><span data-stu-id="2eac5-124">To clear an element of the destination rectangle, use an **xltypeNil** type array element in the source array.</span></span> <span data-ttu-id="2eac5-125">Para limpar todo o retângulo de destino, omita o segundo argumento.</span><span class="sxs-lookup"><span data-stu-id="2eac5-125">To clear the entire destination rectangle, omit the second argument.</span></span> 
  
### <a name="restrictions"></a><span data-ttu-id="2eac5-126">Restriction</span><span class="sxs-lookup"><span data-stu-id="2eac5-126">Restrictions</span></span>

<span data-ttu-id="2eac5-127">**xlSet** não pode ser desfeito.</span><span class="sxs-lookup"><span data-stu-id="2eac5-127">**xlSet** cannot be undone.</span></span> <span data-ttu-id="2eac5-128">Além disso, ele destrói qualquer informação de desfazer que possa estar disponível antes.</span><span class="sxs-lookup"><span data-stu-id="2eac5-128">In addition, it destroys any undo information that may have been available before.</span></span> 
  
<span data-ttu-id="2eac5-129">**xlSet** pode colocar apenas constantes, não fórmulas, em células.</span><span class="sxs-lookup"><span data-stu-id="2eac5-129">**xlSet** can put only constants, not formulas, into cells.</span></span> 
  
<span data-ttu-id="2eac5-130">**xlSet** se comporta como uma função de comando equivalente à classe 3; ou seja, ele está disponível somente dentro de uma DLL quando a DLL é chamada a partir de um objeto, macro, menu, barra de ferramentas, tecla de atalho ou botão **executar** da caixa de diálogo **macro** (acessado da guia **Exibir** na faixa de opções, começando no Excel 2007 e as \*\*ferramentas \*\*menu em versões anteriores).</span><span class="sxs-lookup"><span data-stu-id="2eac5-130">**xlSet** behaves as a Class 3 command-equivalent function; that is, it is available only inside a DLL when the DLL is called from an object, macro, menu, toolbar, shortcut key, or the **Run** button in the **Macro** dialog box (accessed from **View** tab on the ribbon starting in Excel 2007, and the **Tools** menu in earlier versions).</span></span> 
  
## <a name="example"></a><span data-ttu-id="2eac5-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2eac5-131">Example</span></span>

<span data-ttu-id="2eac5-132">O exemplo a seguir preenche B205: B206 com o valor que foi passado de uma macro.</span><span class="sxs-lookup"><span data-stu-id="2eac5-132">The following example fills B205:B206 with the value that was passed in from a macro.</span></span> <span data-ttu-id="2eac5-133">Este exemplo de função de comando requer um argumento e, portanto, só funcionará se for chamado a partir de uma planilha de macro XLM ou de um módulo do VBA usando o método **Application. Run** .</span><span class="sxs-lookup"><span data-stu-id="2eac5-133">This command function example requires an argument, and so will only work if called from an XLM macro sheet, or from a VBA module using the **Application.Run** method.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSetExample(short int iVal)
{
   XLOPER12 xRef, xValue;
   xRef.xltype = xltypeSRef;
   xRef.val.sref.count = 1;
   xRef.val.sref.ref.rwFirst = 204;
   xRef.val.sref.ref.rwLast = 205;
   xRef.val.sref.ref.colFirst = 1;
   xRef.val.sref.ref.colLast = 1;
   xValue.xltype = xltypeInt;
   xValue.val.w = iVal;
   Excel12(xlSet, 0, 2, (LPXLOPER12)&xRef, (LPXLOPER12)&xValue);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="2eac5-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="2eac5-134">See also</span></span>

- [<span data-ttu-id="2eac5-135">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="2eac5-135">xlCoerce</span></span>](xlcoerce.md)
- [<span data-ttu-id="2eac5-136">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="2eac5-136">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

