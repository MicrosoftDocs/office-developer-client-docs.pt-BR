---
title: TempStrConst/TempStr12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr12
- TempStrConst
keywords:
- função tempstr12 [excel 2007], função TempStrConst [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 321c41aa87a3bfa0edc1d77ecc8fbe4b6a6a4730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765450"
---
# <a name="tempstrconsttempstr12"></a><span data-ttu-id="f2de6-104">TempStrConst/TempStr12</span><span class="sxs-lookup"><span data-stu-id="f2de6-104">TempStrConst/TempStr12</span></span>

 <span data-ttu-id="f2de6-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f2de6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f2de6-106">Função de biblioteca Framework que cria um temporário **XLOPER/XLOPER12** que contém uma cadeia de caracteres **xltypeStr** , levando a uma cadeia de caracteres terminada em nulo fonte como entrada.</span><span class="sxs-lookup"><span data-stu-id="f2de6-106">Framework library function that creates a temporary **XLOPER/XLOPER12** that contains an **xltypeStr** string, taking a null-terminated source string as input.</span></span> <span data-ttu-id="f2de6-107">A função aloca um novo buffer de memória e copia a cadeia de caracteres passada para ele.</span><span class="sxs-lookup"><span data-stu-id="f2de6-107">The function allocates a new memory buffer and copies the passed-in string into it.</span></span> <span data-ttu-id="f2de6-108">A cadeia de caracteres de entrada não seja alterada e portanto é declarada como **constante**.</span><span class="sxs-lookup"><span data-stu-id="f2de6-108">The input string is not altered and so is declared as **const**.</span></span>
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a><span data-ttu-id="f2de6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2de6-109">Parameters</span></span>

 <span data-ttu-id="f2de6-110">_str_</span><span class="sxs-lookup"><span data-stu-id="f2de6-110">_str_</span></span>
  
<span data-ttu-id="f2de6-111">Um ponteiro para a cadeia de caracteres fonte terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="f2de6-111">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="f2de6-112">No caso de s **XLOPER**, TempStrConst trunca strings que são maiores do que 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="f2de6-112">In the case of **XLOPER**s, TempStrConst truncates strings that are longer than 255 bytes.</span></span> <span data-ttu-id="f2de6-113">No caso de **XLOPER12**s, TempStr12Const trunca cadeias de caracteres que são mais de 32.767 caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="f2de6-113">In the case of **XLOPER12**s, TempStr12Const truncates strings that are longer than 32,767 Unicode characters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="f2de6-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f2de6-114">Return value</span></span>

<span data-ttu-id="f2de6-115">Retorna uma cadeia de caracteres **xltypeStr** contendo uma cópia do buffer passado na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f2de6-115">Returns an **xltypeStr** string containing a copy of the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f2de6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2de6-116">Remarks</span></span>

<span data-ttu-id="f2de6-117">Observe que a cadeia de caracteres **XLOPER** função Framework, **TempStr**, se comporta de maneira diferente e tenta sobrescrever o primeiro caractere da cadeia de caracteres fornecida com o comprimento da cadeia de caracteres subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f2de6-117">Note that the **XLOPER** string Framework function, **TempStr**, behaves differently and tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="f2de6-118">Isso não é sempre uma segura coisa a fazer: Microsoft Excel pode falhar se passadas uma cadeia de caracteres somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f2de6-118">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> <span data-ttu-id="f2de6-119">A maneira que o trabalho **TempStrConst** e o **TempStr12** agora é substituída dessa maneira de criação de cadeias de caracteres temporárias.</span><span class="sxs-lookup"><span data-stu-id="f2de6-119">This way of creating temporary strings is now deprecated in favor of the way in which both **TempStrConst** and **TempStr12** work.</span></span> <span data-ttu-id="f2de6-120">Portanto, o primeiro caractere da cadeia de caracteres de entrada é tratado como o início da cadeia de caracteres, ou seja, não como um caractere de comprimento ou como um espaço para um caractere de comprimento.</span><span class="sxs-lookup"><span data-stu-id="f2de6-120">Therefore the first character of the input string is treated as the start of the string, that is, not as a length character or as a space for a length character.</span></span> <span data-ttu-id="f2de6-121">Você não deve passar cadeias de caracteres que possuem um caractere de comprimento codificado no início, conforme as consequências poderia ser imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="f2de6-121">You should not pass strings that have a length character encoded at the start, as the consequences could be unpredictable.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f2de6-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f2de6-122">Example</span></span>

<span data-ttu-id="f2de6-123">Este exemplo usa a função **TempStr12** para criar uma cadeia de caracteres para uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f2de6-123">This example uses the **TempStr12** function to create a string for a message box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="f2de6-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2de6-124">See also</span></span>



[<span data-ttu-id="f2de6-125">Funções na biblioteca de estrutura</span><span class="sxs-lookup"><span data-stu-id="f2de6-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

