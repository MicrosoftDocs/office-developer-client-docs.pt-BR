---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- função initframework [Excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34fe8f4a606956b90a0d005b0bc523cea460153f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420749"
---
# <a name="initframework"></a><span data-ttu-id="8790b-104">InitFramework</span><span class="sxs-lookup"><span data-stu-id="8790b-104">InitFramework</span></span>

 <span data-ttu-id="8790b-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8790b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8790b-106">Função da biblioteca da estrutura que inicializa a biblioteca do Framework, que simplesmente inicializa as estruturas de dados de memória do**XLOPER12** de **XLOPER**/ temporários, liberando qualquer memória que já tenha sido alocada.</span><span class="sxs-lookup"><span data-stu-id="8790b-106">Framework library function that initializes the Framework library, which simply initializes the temporary **XLOPER**/ **XLOPER12** memory data structures, freeing any memory that has already been allocated.</span></span> 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a><span data-ttu-id="8790b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8790b-107">Parameters</span></span>

<span data-ttu-id="8790b-108">Essa função não usa argumentos.</span><span class="sxs-lookup"><span data-stu-id="8790b-108">This function takes no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="8790b-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8790b-109">Return value</span></span>

<span data-ttu-id="8790b-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8790b-110">This function does not return a value.</span></span>
  
## <a name="example"></a><span data-ttu-id="8790b-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8790b-111">Example</span></span>

<span data-ttu-id="8790b-112">Este exemplo usa a função **InitFramework** para liberar toda a memória temporária.</span><span class="sxs-lookup"><span data-stu-id="8790b-112">This example uses the **InitFramework** function to free all temporary memory.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="8790b-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="8790b-113">See also</span></span>



[<span data-ttu-id="8790b-114">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="8790b-114">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

