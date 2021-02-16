---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- Função tempstr [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4ccb6f3c764371c35bac12c8c78fede54234a7d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418040"
---
# <a name="tempstr"></a><span data-ttu-id="e571b-104">TempStr</span><span class="sxs-lookup"><span data-stu-id="e571b-104">TempStr</span></span>

 <span data-ttu-id="e571b-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e571b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e571b-106">Função de biblioteca de Estrutura preterida que cria um **XLOPER temporário** contendo uma cadeia de caracteres de byte **xltypeStr.**</span><span class="sxs-lookup"><span data-stu-id="e571b-106">Deprecated Framework library function that creates a temporary **XLOPER** containing an **xltypeStr** byte string.</span></span> <span data-ttu-id="e571b-107">É necessário uma cadeia de caracteres de origem terminada por caractere nulo como entrada.</span><span class="sxs-lookup"><span data-stu-id="e571b-107">It takes a null-terminated source string as input.</span></span> <span data-ttu-id="e571b-108">Ele tenta substituir o primeiro caractere da cadeia de caracteres fornecida pelo comprimento da cadeia de caracteres subsequente.</span><span class="sxs-lookup"><span data-stu-id="e571b-108">It tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="e571b-109">Isso nem sempre é uma coisa segura: o Microsoft Excel pode falhar se passar uma cadeia de caracteres somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e571b-109">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a><span data-ttu-id="e571b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e571b-110">Parameters</span></span>

 <span data-ttu-id="e571b-111">_str_</span><span class="sxs-lookup"><span data-stu-id="e571b-111">_str_</span></span>
  
<span data-ttu-id="e571b-112">Um ponteiro para a cadeia de caracteres de origem terminada por caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="e571b-112">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="e571b-113">**TempStr** trunca cadeias de caracteres que têm mais de 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="e571b-113">**TempStr** truncates strings that are longer than 255 bytes.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="e571b-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e571b-114">Return value</span></span>

<span data-ttu-id="e571b-115">Retorna uma **cadeia de caracteres xltypeStr** que contém um ponteiro para o buffer de cadeia de caracteres passado.</span><span class="sxs-lookup"><span data-stu-id="e571b-115">Returns an **xltypeStr** string containing a pointer to the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e571b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e571b-116">Remarks</span></span>

<span data-ttu-id="e571b-117">This way of creating temporary strings is now deprecated in favor of the way in which both [TempStrConst and TempStr12](tempstrconst-tempstr12.md) work.</span><span class="sxs-lookup"><span data-stu-id="e571b-117">This way of creating temporary strings is now deprecated in favor of the way in which both [TempStrConst and TempStr12](tempstrconst-tempstr12.md) work.</span></span> <span data-ttu-id="e571b-118">Essas funções alocam um novo buffer de memória e copiam a cadeia de caracteres passada nele.</span><span class="sxs-lookup"><span data-stu-id="e571b-118">These functions allocate a new memory buffer and copy the passed-in string into it.</span></span> <span data-ttu-id="e571b-119">As cadeias de caracteres de entrada **para TempStrConst** e **TempStr12** não são alteradas e, portanto, são declaradas como **constante**.</span><span class="sxs-lookup"><span data-stu-id="e571b-119">The input strings for **TempStrConst** and **TempStr12** are not altered and so are declared as **const**.</span></span> <span data-ttu-id="e571b-120">Por outro lado, a cadeia de caracteres de entrada **para TempStr** é alterada e, portanto, não pode ser declarada como **constante**.</span><span class="sxs-lookup"><span data-stu-id="e571b-120">In contrast, the input string to **TempStr** is altered and so cannot be declared as **const**.</span></span> <span data-ttu-id="e571b-121">O primeiro caractere da cadeia de caracteres de entrada é tratado como espaço para um caractere de comprimento e é substituído por essa função.</span><span class="sxs-lookup"><span data-stu-id="e571b-121">The first character of the input string is treated as space for a length character and is overwritten by this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e571b-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e571b-122">See also</span></span>



[<span data-ttu-id="e571b-123">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="e571b-123">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

