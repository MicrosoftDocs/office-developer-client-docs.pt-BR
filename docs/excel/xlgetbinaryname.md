---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- função xlgetbinaryname [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d2332967e798b43a350c0733cd7398e2a921add6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765470"
---
# <a name="xlgetbinaryname"></a><span data-ttu-id="7c4d2-104">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="7c4d2-104">xlGetBinaryName</span></span>

<span data-ttu-id="7c4d2-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7c4d2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7c4d2-106">Usado para retornar uma alça de dados salvos pela [função xlDefineBinaryName](xldefinebinaryname.md).</span><span class="sxs-lookup"><span data-stu-id="7c4d2-106">Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md).</span></span> <span data-ttu-id="7c4d2-107">Dados com um nome definido de binário é salvo com a pasta de trabalho e podem ser acessados pelo nome, a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="7c4d2-107">Data with a defined binary name is saved with the workbook and can be accessed by name at any time.</span></span> <span data-ttu-id="7c4d2-108">Para obter mais informações, consulte "Binário" nomeie a limitação de escopo em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="7c4d2-108">For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a><span data-ttu-id="7c4d2-109">Par�metros</span><span class="sxs-lookup"><span data-stu-id="7c4d2-109">Parameters</span></span>

<span data-ttu-id="7c4d2-110">_pxRes_ (**xltypeBigData** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="7c4d2-110">_pxRes_ (**xltypeBigData** or **xltypeErr**)</span></span>
  
<span data-ttu-id="7c4d2-111">Estrutura de Bigdata especificando que um erro ou os dados recuperados é os dados não pôde ser recuperada ou o nome não está definido.</span><span class="sxs-lookup"><span data-stu-id="7c4d2-111">Bigdata structure specifying the retrieved data or an error is the data could not be retrieved or the name is not defined.</span></span> <span data-ttu-id="7c4d2-112">Quando a função retorna, o membro de **hdata** da **XLOPER**/ **XLOPER12** contém uma alça para os dados nomeadas.</span><span class="sxs-lookup"><span data-stu-id="7c4d2-112">When the function returns, the **hdata** member of the **XLOPER**/ **XLOPER12** contains a handle for the named data.</span></span>  <span data-ttu-id="7c4d2-113">_pxRes_ deve ser liberada em uma chamada para **xlFree** quando não são mais necessários.</span><span class="sxs-lookup"><span data-stu-id="7c4d2-113">_pxRes_ should be freed in a call to **xlFree** when no longer required.</span></span> 
  
<span data-ttu-id="7c4d2-114">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="7c4d2-114">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="7c4d2-115">Uma cadeia de caracteres especificando o nome dos dados.</span><span class="sxs-lookup"><span data-stu-id="7c4d2-115">A string specifying the name of the data.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7c4d2-116">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="7c4d2-116">Remarks</span></span>

<span data-ttu-id="7c4d2-117">O Microsoft Excel possui o identificador de memória retornado em **hdata**.</span><span class="sxs-lookup"><span data-stu-id="7c4d2-117">Microsoft Excel owns the memory handle returned in **hdata**.</span></span> <span data-ttu-id="7c4d2-118">No Windows, o identificador é uma alça de memória global (alocada pela função **GlobalAlloc** ).</span><span class="sxs-lookup"><span data-stu-id="7c4d2-118">In Windows, the handle is a global memory handle (allocated by the **GlobalAlloc** function).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c4d2-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c4d2-119">See also</span></span>

- [<span data-ttu-id="7c4d2-120">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="7c4d2-120">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
- [<span data-ttu-id="7c4d2-121">Funções da API C que podem ser chamadas apenas por um DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="7c4d2-121">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

