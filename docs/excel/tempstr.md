---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- função tempstr [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ce9399168d5b94d10481d2d0b5b69dd2e1d1d2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765447"
---
# <a name="tempstr"></a><span data-ttu-id="cf226-104">TempStr</span><span class="sxs-lookup"><span data-stu-id="cf226-104">TempStr</span></span>

 <span data-ttu-id="cf226-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cf226-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cf226-106">Função preterida da biblioteca Framework que cria um temporário que contém uma cadeia de caracteres de byte **xltypeStr** **XLOPER** .</span><span class="sxs-lookup"><span data-stu-id="cf226-106">Deprecated Framework library function that creates a temporary **XLOPER** containing an **xltypeStr** byte string.</span></span> <span data-ttu-id="cf226-107">Ele aceita uma cadeia de caracteres terminada em nulo fonte como entrada.</span><span class="sxs-lookup"><span data-stu-id="cf226-107">It takes a null-terminated source string as input.</span></span> <span data-ttu-id="cf226-108">Ele tentará substituir o primeiro caractere da cadeia de caracteres fornecida com o comprimento da cadeia de caracteres subsequentes.</span><span class="sxs-lookup"><span data-stu-id="cf226-108">It tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="cf226-109">Isso não é sempre uma segura coisa a fazer: Microsoft Excel pode falhar se passadas uma cadeia de caracteres somente leitura.</span><span class="sxs-lookup"><span data-stu-id="cf226-109">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a><span data-ttu-id="cf226-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf226-110">Parameters</span></span>

 <span data-ttu-id="cf226-111">_str_</span><span class="sxs-lookup"><span data-stu-id="cf226-111">_str_</span></span>
  
<span data-ttu-id="cf226-112">Um ponteiro para a cadeia de caracteres fonte terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="cf226-112">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="cf226-113">**TempStr** trunca strings que são maiores do que 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="cf226-113">**TempStr** truncates strings that are longer than 255 bytes.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="cf226-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="cf226-114">Return value</span></span>

<span data-ttu-id="cf226-115">Retorna uma cadeia de caracteres **xltypeStr** contendo um ponteiro para o buffer passado na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cf226-115">Returns an **xltypeStr** string containing a pointer to the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cf226-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf226-116">Remarks</span></span>

<span data-ttu-id="cf226-117">A maneira em que ambos os trabalhos de [TempStrConst e TempStr12](tempstrconst-tempstr12.md) agora é substituída dessa maneira de criação de cadeias de caracteres temporárias.</span><span class="sxs-lookup"><span data-stu-id="cf226-117">This way of creating temporary strings is now deprecated in favor of the way in which both [TempStrConst and TempStr12](tempstrconst-tempstr12.md) work.</span></span> <span data-ttu-id="cf226-118">Essas funções alocar um novo buffer de memória e copiem a cadeia de caracteres passada para ele.</span><span class="sxs-lookup"><span data-stu-id="cf226-118">These functions allocate a new memory buffer and copy the passed-in string into it.</span></span> <span data-ttu-id="cf226-119">As cadeias de caracteres de entrada para **TempStrConst** e **TempStr12** não forem alteradas e portanto são declaradas como **constante**.</span><span class="sxs-lookup"><span data-stu-id="cf226-119">The input strings for **TempStrConst** and **TempStr12** are not altered and so are declared as **const**.</span></span> <span data-ttu-id="cf226-120">Por outro lado, a sequência de entrada para **TempStr** for alterada e não pode ser declarada como **constante**.</span><span class="sxs-lookup"><span data-stu-id="cf226-120">In contrast, the input string to **TempStr** is altered and so cannot be declared as **const**.</span></span> <span data-ttu-id="cf226-121">O primeiro caractere da cadeia de caracteres de entrada é tratado como espaço para um caractere de comprimento e será substituído por essa função.</span><span class="sxs-lookup"><span data-stu-id="cf226-121">The first character of the input string is treated as space for a length character and is overwritten by this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf226-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf226-122">See also</span></span>



[<span data-ttu-id="cf226-123">Funções na biblioteca de estrutura</span><span class="sxs-lookup"><span data-stu-id="cf226-123">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

