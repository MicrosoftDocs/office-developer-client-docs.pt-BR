---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- função xlsheetid [excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e4e184d4e456ffe26292fe31b1b41463834216f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765481"
---
# <a name="xlsheetid"></a><span data-ttu-id="30266-104">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="30266-104">xlSheetId</span></span>

<span data-ttu-id="30266-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="30266-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="30266-106">Localiza a ID de folha de uma planilha nomeada para construir as referências externas.</span><span class="sxs-lookup"><span data-stu-id="30266-106">Finds the sheet ID of a named sheet in order to construct external references.</span></span>
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a><span data-ttu-id="30266-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30266-107">Parameters</span></span>

<span data-ttu-id="30266-108">_pxSheetName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="30266-108">_pxSheetName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="30266-109">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="30266-109">(Optional).</span></span> <span data-ttu-id="30266-110">O nome do catálogo e folha que você deseja saber sobre.</span><span class="sxs-lookup"><span data-stu-id="30266-110">The name of the book and sheet you want to find out about.</span></span> <span data-ttu-id="30266-111">Se for omitido, a função **xlSheetId** retorna a ID de folha da planilha ativa (frente).</span><span class="sxs-lookup"><span data-stu-id="30266-111">If omitted, the **xlSheetId** function returns the sheet ID of the active (front) sheet.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="30266-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="30266-112">Return value</span></span>

<span data-ttu-id="30266-113">Retorna a ID de folha no _pxRes -\>val.mref.idSheet_.</span><span class="sxs-lookup"><span data-stu-id="30266-113">Returns the sheet ID in  _pxRes-\>val.mref.idSheet_.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="30266-114">O _pxRes -\>val.mref.lpmref_ ponteiro de matriz é definido como NULL após essa chamada para que não é necessário chamar **xlFree** para liberar a memória que normalmente contém esse tipo, embora seja completamente seguro de fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="30266-114">The  _pxRes-\>val.mref.lpmref_ array pointer is set to NULL after this call so that there is no need to call **xlFree** to release the memory that this type normally contains, although it is completely safe to do so.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="30266-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="30266-115">Remarks</span></span>

<span data-ttu-id="30266-116">A pasta de trabalho contendo a planilha especificada deve ser aberta para usar esta função.</span><span class="sxs-lookup"><span data-stu-id="30266-116">The workbook containing the specified sheet must be open to use this function.</span></span> <span data-ttu-id="30266-117">Não é possível construir uma referência a uma pasta de trabalho não aberta de uma DLL.</span><span class="sxs-lookup"><span data-stu-id="30266-117">There is no way to construct a reference to an unopened workbook from a DLL.</span></span> <span data-ttu-id="30266-118">Para obter mais informações sobre como usar o **xlSheetId** para construir referências, consulte [Gerenciamento de memória no Excel](memory-management-in-excel.md) para obter exemplos de construção de **xltypeRef** .</span><span class="sxs-lookup"><span data-stu-id="30266-118">For more information about using **xlSheetId** to construct references, see [Memory Management in Excel](memory-management-in-excel.md) for examples of **xltypeRef** construction.</span></span> 
  
## <a name="example"></a><span data-ttu-id="30266-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="30266-119">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="30266-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="30266-120">See also</span></span>

- [<span data-ttu-id="30266-121">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="30266-121">xlSheetNm</span></span>](xlsheetnm.md)
- [<span data-ttu-id="30266-122">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="30266-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

