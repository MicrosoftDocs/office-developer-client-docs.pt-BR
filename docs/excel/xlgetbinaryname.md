---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- Função xlgetbinaryname [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6d063213e3f83451e8a072e71f0878174214f73e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412461"
---
# <a name="xlgetbinaryname"></a><span data-ttu-id="43ef4-104">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="43ef4-104">xlGetBinaryName</span></span>

<span data-ttu-id="43ef4-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="43ef4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="43ef4-106">Usado para retornar um alça para dados salvos pela [função xlDefineBinaryName](xldefinebinaryname.md).</span><span class="sxs-lookup"><span data-stu-id="43ef4-106">Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md).</span></span> <span data-ttu-id="43ef4-107">Os dados com um nome binário definido são salvos com a agenda e podem ser acessados por nome a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="43ef4-107">Data with a defined binary name is saved with the workbook and can be accessed by name at any time.</span></span> <span data-ttu-id="43ef4-108">Para obter mais informações, consulte "Limitação de escopo de nome binário" em [Problemas conhecidos no desenvolvimento de XLL do Excel.](known-issues-in-excel-xll-development.md)</span><span class="sxs-lookup"><span data-stu-id="43ef4-108">For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a><span data-ttu-id="43ef4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43ef4-109">Parameters</span></span>

<span data-ttu-id="43ef4-110">_pxRes_ (**xltypeBigData** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="43ef4-110">_pxRes_ (**xltypeBigData** or **xltypeErr**)</span></span>
  
<span data-ttu-id="43ef4-111">A estrutura bigdata especificando os dados recuperados ou um erro é que os dados não puderam ser recuperados ou o nome não foi definido.</span><span class="sxs-lookup"><span data-stu-id="43ef4-111">Bigdata structure specifying the retrieved data or an error is the data could not be retrieved or the name is not defined.</span></span> <span data-ttu-id="43ef4-112">Quando a função retorna, o **membro hdata** do **XLOPER** /  **XLOPER12** contém um identificador para os dados nomeados.</span><span class="sxs-lookup"><span data-stu-id="43ef4-112">When the function returns, the **hdata** member of the **XLOPER**/ **XLOPER12** contains a handle for the named data.</span></span>  <span data-ttu-id="43ef4-113">_PxRes_ devem ser liberados em uma chamada **para xlFree** quando não for mais necessário.</span><span class="sxs-lookup"><span data-stu-id="43ef4-113">_pxRes_ should be freed in a call to **xlFree** when no longer required.</span></span> 
  
<span data-ttu-id="43ef4-114">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="43ef4-114">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="43ef4-115">Uma cadeia de caracteres especificando o nome dos dados.</span><span class="sxs-lookup"><span data-stu-id="43ef4-115">A string specifying the name of the data.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43ef4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="43ef4-116">Remarks</span></span>

<span data-ttu-id="43ef4-117">O Microsoft Excel possui o alça de memória retornado em **hdata.**</span><span class="sxs-lookup"><span data-stu-id="43ef4-117">Microsoft Excel owns the memory handle returned in **hdata**.</span></span> <span data-ttu-id="43ef4-118">No Windows, o alça é um alça de memória global (alocado pela **função GlobalAlloc).**</span><span class="sxs-lookup"><span data-stu-id="43ef4-118">In Windows, the handle is a global memory handle (allocated by the **GlobalAlloc** function).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="43ef4-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="43ef4-119">See also</span></span>

- [<span data-ttu-id="43ef4-120">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="43ef4-120">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
- [<span data-ttu-id="43ef4-121">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="43ef4-121">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

