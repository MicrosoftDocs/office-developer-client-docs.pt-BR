---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- função xlsheetid [Excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2ca1bb478c5c985ad7032e30ed0cfe3aef31406
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310301"
---
# <a name="xlsheetid"></a><span data-ttu-id="6e17c-104">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="6e17c-104">xlSheetId</span></span>

<span data-ttu-id="6e17c-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6e17c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6e17c-106">Localiza a ID de uma folha nomeada para criar referências externas.</span><span class="sxs-lookup"><span data-stu-id="6e17c-106">Finds the sheet ID of a named sheet in order to construct external references.</span></span>
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a><span data-ttu-id="6e17c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e17c-107">Parameters</span></span>

<span data-ttu-id="6e17c-108">_pxSheetName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="6e17c-108">_pxSheetName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="6e17c-109">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="6e17c-109">(Optional).</span></span> <span data-ttu-id="6e17c-110">O nome do livro e planilha que você deseja descobrir.</span><span class="sxs-lookup"><span data-stu-id="6e17c-110">The name of the book and sheet you want to find out about.</span></span> <span data-ttu-id="6e17c-111">Se for omitido, a função **xlSheetId** retornará a ID de planilha da planilha ativa (frontal).</span><span class="sxs-lookup"><span data-stu-id="6e17c-111">If omitted, the **xlSheetId** function returns the sheet ID of the active (front) sheet.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="6e17c-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6e17c-112">Return value</span></span>

<span data-ttu-id="6e17c-113">Retorna o ID de planilha em _pxRes\>-Val. mref. idSheet_.</span><span class="sxs-lookup"><span data-stu-id="6e17c-113">Returns the sheet ID in  _pxRes-\>val.mref.idSheet_.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6e17c-114">O ponteiro de matriz _pxRes-\>Val. mref. lpmref_ é definido como nulo após esta chamada, de modo que não haja necessidade de chamar **xlFree** para liberar a memória que esse tipo normalmente contém, embora seja totalmente seguro.</span><span class="sxs-lookup"><span data-stu-id="6e17c-114">The  _pxRes-\>val.mref.lpmref_ array pointer is set to NULL after this call so that there is no need to call **xlFree** to release the memory that this type normally contains, although it is completely safe to do so.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6e17c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e17c-115">Remarks</span></span>

<span data-ttu-id="6e17c-116">A pasta de trabalho que contém a folha especificada deve estar aberta para usar essa função.</span><span class="sxs-lookup"><span data-stu-id="6e17c-116">The workbook containing the specified sheet must be open to use this function.</span></span> <span data-ttu-id="6e17c-117">Não há como criar uma referência a uma pasta de trabalho não aberta de uma DLL.</span><span class="sxs-lookup"><span data-stu-id="6e17c-117">There is no way to construct a reference to an unopened workbook from a DLL.</span></span> <span data-ttu-id="6e17c-118">Para obter mais informações sobre como usar o **xlSheetId** para construir referências, confira [Gerenciamento de memória no Excel](memory-management-in-excel.md) para obter exemplos de construção **xltypeRef** .</span><span class="sxs-lookup"><span data-stu-id="6e17c-118">For more information about using **xlSheetId** to construct references, see [Memory Management in Excel](memory-management-in-excel.md) for examples of **xltypeRef** construction.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6e17c-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6e17c-119">Example</span></span>

 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetIdExample(void)
{       
   XLOPER12 xSheetName, xRes;
   xSheetName.xltype = xltypeStr;
   xSheetName.val.str = L"\022[BOOK1.XLSX]Sheet1";
   Excel12(xlSheetId, &xRes, 1, (LPXLOPER12)&xSheetName);
   Excel12f(xlcAlert, 0, 1, TempNum12(xRes.val.mref.idSheet));
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="6e17c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e17c-120">See also</span></span>

- [<span data-ttu-id="6e17c-121">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="6e17c-121">xlSheetNm</span></span>](xlsheetnm.md)
- [<span data-ttu-id="6e17c-122">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="6e17c-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

