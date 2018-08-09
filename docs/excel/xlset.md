---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- função xlSet [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 63f50e441f5d851677f36754a17bcd6403705239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765493"
---
# <a name="xlset"></a><span data-ttu-id="3d90a-104">xlSet</span><span class="sxs-lookup"><span data-stu-id="3d90a-104">xlSet</span></span>

<span data-ttu-id="3d90a-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3d90a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3d90a-106">Coloca valores de constantes em intervalos de células ou muito rapidamente.</span><span class="sxs-lookup"><span data-stu-id="3d90a-106">Puts constant values into cells or ranges very quickly.</span></span> <span data-ttu-id="3d90a-107">Para obter mais informações, consulte "xlSet e pastas de trabalho com fórmulas de matriz" em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="3d90a-107">For more information, see "xlSet and Workbooks with Array Formulas" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a><span data-ttu-id="3d90a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d90a-108">Parameters</span></span>

<span data-ttu-id="3d90a-109">_pxReference_ (**xltypeRef** ou **xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="3d90a-109">_pxReference_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="3d90a-110">Uma referência retangular descrevendo o destino de uma ou mais células.</span><span class="sxs-lookup"><span data-stu-id="3d90a-110">A rectangular reference describing the target cell or cells.</span></span> <span data-ttu-id="3d90a-111">A referência deve descrever células adjacentes, portanto isso em um **xltypeRef** `val.mref.lpmref->count` deve ser definida como 1.</span><span class="sxs-lookup"><span data-stu-id="3d90a-111">The reference must describe adjacent cells, so that in an **xltypeRef** `val.mref.lpmref->count` must be set to 1.</span></span> 
  
<span data-ttu-id="3d90a-112">_pxValue_</span><span class="sxs-lookup"><span data-stu-id="3d90a-112">_pxValue_</span></span>
  
<span data-ttu-id="3d90a-113">O valor ou valores sejam colocadas em uma ou mais células.</span><span class="sxs-lookup"><span data-stu-id="3d90a-113">The value or values to be placed into the cell or cells.</span></span> <span data-ttu-id="3d90a-114">Para obter mais informações, consulte a seção "Comentários".</span><span class="sxs-lookup"><span data-stu-id="3d90a-114">For more information, see the "Remarks" section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3d90a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d90a-115">Remarks</span></span>

### <a name="pxvalue-argument"></a><span data-ttu-id="3d90a-116">argumento pxValue</span><span class="sxs-lookup"><span data-stu-id="3d90a-116">pxValue argument</span></span>

<span data-ttu-id="3d90a-117">_pxValue_ pode ser um valor ou uma matriz.</span><span class="sxs-lookup"><span data-stu-id="3d90a-117">_pxValue_ can either be a value or an array.</span></span> <span data-ttu-id="3d90a-118">Se for um valor, o intervalo de destino inteira é preenchido com esse valor.</span><span class="sxs-lookup"><span data-stu-id="3d90a-118">If it is a value, the entire destination range is filled with that value.</span></span> <span data-ttu-id="3d90a-119">Se for uma matriz (**xltypeMulti**), os elementos da matriz são colocados nos locais correspondentes no retângulo.</span><span class="sxs-lookup"><span data-stu-id="3d90a-119">If it is an array (**xltypeMulti**), the elements of the array are put into the corresponding locations in the rectangle.</span></span>
  
<span data-ttu-id="3d90a-120">Se você usar uma matriz horizontal para o segundo argumento, ele é duplicado para baixo para preencher todo o retângulo.</span><span class="sxs-lookup"><span data-stu-id="3d90a-120">If you use a horizontal array for the second argument, it is duplicated down to fill the entire rectangle.</span></span> <span data-ttu-id="3d90a-121">Se você usar uma matriz vertical, ele é duplicado direita para preencher o retângulo inteiro.</span><span class="sxs-lookup"><span data-stu-id="3d90a-121">If you use a vertical array, it is duplicated right to fill the entire rectangle.</span></span> <span data-ttu-id="3d90a-122">Se você usar uma matriz retangular e é muito pequeno para o intervalo retangular que você deseja colocá-lo no, aquele intervalo é preenchido com s **# N/d**.</span><span class="sxs-lookup"><span data-stu-id="3d90a-122">If you use a rectangular array, and it is too small for the rectangular range you want to put it in, that range is padded with **#N/A**s.</span></span>
  
<span data-ttu-id="3d90a-123">Se o intervalo de destino for menor que a matriz de origem, os valores são copiados em até os limites do intervalo de destino e os dados extras serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="3d90a-123">If the target range is smaller than the source array, the values are copied in up to the limits of the target range and the extra data are ignored.</span></span>
  
<span data-ttu-id="3d90a-124">Para limpar um elemento do retângulo de destino, use um elemento de matriz do tipo **xltypeNil** da matriz de origem.</span><span class="sxs-lookup"><span data-stu-id="3d90a-124">To clear an element of the destination rectangle, use an **xltypeNil** type array element in the source array.</span></span> <span data-ttu-id="3d90a-125">Para limpar o retângulo de destino inteira, omita o segundo argumento.</span><span class="sxs-lookup"><span data-stu-id="3d90a-125">To clear the entire destination rectangle, omit the second argument.</span></span> 
  
### <a name="restrictions"></a><span data-ttu-id="3d90a-126">Restrições</span><span class="sxs-lookup"><span data-stu-id="3d90a-126">Restrictions</span></span>

<span data-ttu-id="3d90a-127">**xlSet** não pode ser desfeita.</span><span class="sxs-lookup"><span data-stu-id="3d90a-127">**xlSet** cannot be undone.</span></span> <span data-ttu-id="3d90a-128">Além disso, ele destrua qualquer informação de desfazer que pode ter sido disponível antes.</span><span class="sxs-lookup"><span data-stu-id="3d90a-128">In addition, it destroys any undo information that may have been available before.</span></span> 
  
<span data-ttu-id="3d90a-129">**xlSet** pode colocar apenas constantes, não fórmulas em células.</span><span class="sxs-lookup"><span data-stu-id="3d90a-129">**xlSet** can put only constants, not formulas, into cells.</span></span> 
  
<span data-ttu-id="3d90a-130">**xlSet** se comporta como uma função equivalente de comando de classe 3; ou seja, ele estará disponível somente dentro de uma DLL quando a DLL é chamada a partir de um objeto, macro, menu, barra de ferramentas, tecla de atalho ou no botão **Executar** na caixa de diálogo **Macro** (acessada a partir da guia **Exibir** da faixa de opções inicial no Excel 2007 e as ferramentas de ** **menu em versões anteriores).</span><span class="sxs-lookup"><span data-stu-id="3d90a-130">**xlSet** behaves as a Class 3 command-equivalent function; that is, it is available only inside a DLL when the DLL is called from an object, macro, menu, toolbar, shortcut key, or the **Run** button in the **Macro** dialog box (accessed from **View** tab on the ribbon starting in Excel 2007, and the **Tools** menu in earlier versions).</span></span> 
  
## <a name="example"></a><span data-ttu-id="3d90a-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3d90a-131">Example</span></span>

<span data-ttu-id="3d90a-132">O exemplo a seguir preenche B205:B206 com o valor passado em de uma macro.</span><span class="sxs-lookup"><span data-stu-id="3d90a-132">The following example fills B205:B206 with the value that was passed in from a macro.</span></span> <span data-ttu-id="3d90a-133">Exemplo da função este comando requer um argumento e portanto funcionará somente se for chamado a partir de uma folha de macro XLM ou um módulo do VBA usando o método Application **Run** .</span><span class="sxs-lookup"><span data-stu-id="3d90a-133">This command function example requires an argument, and so will only work if called from an XLM macro sheet, or from a VBA module using the **Application.Run** method.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="3d90a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d90a-134">See also</span></span>

- [<span data-ttu-id="3d90a-135">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="3d90a-135">xlCoerce</span></span>](xlcoerce.md)
- [<span data-ttu-id="3d90a-136">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="3d90a-136">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

