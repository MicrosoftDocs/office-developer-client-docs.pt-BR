---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- função xlDefineBinaryName [Excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3c7fc4f6b6fc7179c1ca84043895273b2781f8b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310210"
---
# <a name="xldefinebinaryname"></a><span data-ttu-id="4be35-104">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="4be35-104">xlDefineBinaryName</span></span>

 <span data-ttu-id="4be35-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4be35-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4be35-106">Usado para alocar armazenamento persistente para um **xltypeBigData** **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="4be35-106">Used to allocate persistent storage for an **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="4be35-107">Os dados com um nome binário definido são salvos com a pasta de trabalho e podem ser acessados pelo nome a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="4be35-107">Data with a defined binary name is saved with the workbook, and can be accessed by name at any time.</span></span> <span data-ttu-id="4be35-108">Para saber mais, confira "limitação de escopo de nome binário" em [problemas conhecidos no desenvolvimento XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="4be35-108">For more information, see "Binary Name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a><span data-ttu-id="4be35-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4be35-109">Parameters</span></span>

 <span data-ttu-id="4be35-110">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="4be35-110">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="4be35-111">Uma cadeia de caracteres especificando o nome dos dados.</span><span class="sxs-lookup"><span data-stu-id="4be35-111">A string specifying the name of the data.</span></span> <span data-ttu-id="4be35-112">A cadeia de caracteres está sujeita às mesmas restrições de nomenclatura que os nomes definidos.</span><span class="sxs-lookup"><span data-stu-id="4be35-112">The string is subject to the same naming restrictions as defined names.</span></span>
  
 <span data-ttu-id="4be35-113">_pxData_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="4be35-113">_pxData_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="4be35-114">Estrutura bigdata que especifica os dados a serem armazenados.</span><span class="sxs-lookup"><span data-stu-id="4be35-114">Bigdata structure specifying the data to be stored.</span></span> <span data-ttu-id="4be35-115">Ao chamar essa função, o membro **lpbData** da estrutura **bigdata** deve apontar para os dados para os quais o nome está sendo definido, e o membro **cbData** deve conter o tamanho dos dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="4be35-115">When you call this function, the **lpbData** member of the **bigdata** structure should point to the data for which the name is being defined, and the **cbData** member should contain the length of the data in bytes.</span></span> 
  
<span data-ttu-id="4be35-116">Se o argumento _pxData_ não for especificado (**xltypeMissing**), a alocação nomeada especificada por _pxName_ será excluída.</span><span class="sxs-lookup"><span data-stu-id="4be35-116">If the  _pxData_ argument is not specified (**xltypeMissing**), the named allocation specified by  _pxName_ is deleted.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4be35-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="4be35-117">See also</span></span>



[<span data-ttu-id="4be35-118">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="4be35-118">xlGetBinaryName</span></span>](xlgetbinaryname.md)


[<span data-ttu-id="4be35-119">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="4be35-119">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="4be35-120">Problemas conhecidos no desenvolvimento do Excel XLL </span><span class="sxs-lookup"><span data-stu-id="4be35-120">Known Issues in Excel XLL Development</span></span>](known-issues-in-excel-xll-development.md)

