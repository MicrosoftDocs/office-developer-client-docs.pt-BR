---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- função xlDefineBinaryName [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 14515cc262ea398a9f200c0de3a1f6b64c758b3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765454"
---
# <a name="xldefinebinaryname"></a><span data-ttu-id="bcbad-104">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="bcbad-104">xlDefineBinaryName</span></span>

 <span data-ttu-id="bcbad-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bcbad-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bcbad-106">Usado para alocar armazenamento persistente para um **xltypeBigData** **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="bcbad-106">Used to allocate persistent storage for an **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="bcbad-107">Dados com um nome definido de binário é salvo com a pasta de trabalho e podem ser acessados pelo nome, a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="bcbad-107">Data with a defined binary name is saved with the workbook, and can be accessed by name at any time.</span></span> <span data-ttu-id="bcbad-108">Para obter mais informações, consulte "Binário nome escopo limitação" em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="bcbad-108">For more information, see "Binary Name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a><span data-ttu-id="bcbad-109">Par�metros</span><span class="sxs-lookup"><span data-stu-id="bcbad-109">Parameters</span></span>

 <span data-ttu-id="bcbad-110">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="bcbad-110">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="bcbad-111">Uma cadeia de caracteres especificando o nome dos dados.</span><span class="sxs-lookup"><span data-stu-id="bcbad-111">A string specifying the name of the data.</span></span> <span data-ttu-id="bcbad-112">A cadeia de caracteres está sujeito a mesma nomes definidos como restrições de nomeação.</span><span class="sxs-lookup"><span data-stu-id="bcbad-112">The string is subject to the same naming restrictions as defined names.</span></span>
  
 <span data-ttu-id="bcbad-113">_pxData_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="bcbad-113">_pxData_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="bcbad-114">Estrutura de Bigdata especificando os dados a serem armazenados.</span><span class="sxs-lookup"><span data-stu-id="bcbad-114">Bigdata structure specifying the data to be stored.</span></span> <span data-ttu-id="bcbad-115">Quando você chamar essa função, o membro **lpbData** da estrutura **bigdata** deve apontar para os dados para o qual o nome está definido e o membro **cbData diferente** deve conter o tamanho dos dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="bcbad-115">When you call this function, the **lpbData** member of the **bigdata** structure should point to the data for which the name is being defined, and the **cbData** member should contain the length of the data in bytes.</span></span> 
  
<span data-ttu-id="bcbad-116">Se o argumento _pxData_ não for especificado (**xltypeMissing**), a alocação nomeada especificada por _pxName_ é excluída.</span><span class="sxs-lookup"><span data-stu-id="bcbad-116">If the  _pxData_ argument is not specified (**xltypeMissing**), the named allocation specified by  _pxName_ is deleted.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bcbad-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcbad-117">See also</span></span>



[<span data-ttu-id="bcbad-118">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="bcbad-118">xlGetBinaryName</span></span>](xlgetbinaryname.md)


[<span data-ttu-id="bcbad-119">Funções da API C que podem ser chamadas apenas por um DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="bcbad-119">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="bcbad-120">Problemas conhecidos no desenvolvimento de XLL do Excel</span><span class="sxs-lookup"><span data-stu-id="bcbad-120">Known Issues in Excel XLL Development</span></span>](known-issues-in-excel-xll-development.md)

