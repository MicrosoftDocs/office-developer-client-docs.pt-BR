---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- função initframework [excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2d7e3286d794d6f21da9ef83ca44d18ec242c063
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765371"
---
# <a name="initframework"></a><span data-ttu-id="1d08a-104">InitFramework</span><span class="sxs-lookup"><span data-stu-id="1d08a-104">InitFramework</span></span>

 <span data-ttu-id="1d08a-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1d08a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1d08a-106">Função da biblioteca de Framework que inicializa a biblioteca de Framework, que simplesmente inicializa temporário **XLOPER**/ **XLOPER12** estruturas de dados de memória, dispensando qualquer memória que já foi alocada.</span><span class="sxs-lookup"><span data-stu-id="1d08a-106">Framework library function that initializes the Framework library, which simply initializes the temporary **XLOPER**/ **XLOPER12** memory data structures, freeing any memory that has already been allocated.</span></span> 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a><span data-ttu-id="1d08a-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="1d08a-107">Parameters</span></span>

<span data-ttu-id="1d08a-108">Essa função não assume nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="1d08a-108">This function takes no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="1d08a-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1d08a-109">Return value</span></span>

<span data-ttu-id="1d08a-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1d08a-110">This function does not return a value.</span></span>
  
## <a name="example"></a><span data-ttu-id="1d08a-111">Example</span><span class="sxs-lookup"><span data-stu-id="1d08a-111">Example</span></span>

<span data-ttu-id="1d08a-112">Este exemplo usa a função **InitFramework** para liberar memória temporária todos.</span><span class="sxs-lookup"><span data-stu-id="1d08a-112">This example uses the **InitFramework** function to free all temporary memory.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="1d08a-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d08a-113">See also</span></span>



[<span data-ttu-id="1d08a-114">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="1d08a-114">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

