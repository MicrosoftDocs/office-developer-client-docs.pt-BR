---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- função debugprintf [Excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424795"
---
# <a name="debugprintf"></a><span data-ttu-id="48582-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="48582-104">debugPrintf</span></span>

<span data-ttu-id="48582-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="48582-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="48582-106">A função da biblioteca de estrutura que grava uma cadeia de caracteres byte terminada em nulo no depurador ativo por meio da função SDK do Windows **OutputDebugStringa**.</span><span class="sxs-lookup"><span data-stu-id="48582-106">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**.</span></span> <span data-ttu-id="48582-107">Se o aplicativo não tiver nenhum depurador, o depurador do sistema exibe a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="48582-107">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="48582-108">Se o aplicativo não tiver nenhum depurador e o depurador do sistema não estiver ativo, o **debugPrintf** não fará nada.</span><span class="sxs-lookup"><span data-stu-id="48582-108">If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="48582-109">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="48582-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="48582-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48582-110">Parameters</span></span>

 <span data-ttu-id="48582-111">_lpFormat (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="48582-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="48582-112">A cadeia de caracteres de formato, que segue a sintaxe e as regras usadas com a função **sprintf** .</span><span class="sxs-lookup"><span data-stu-id="48582-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="48582-113">_argumento_</span><span class="sxs-lookup"><span data-stu-id="48582-113">_arguments_</span></span>
  
<span data-ttu-id="48582-114">Zero ou mais argumentos para corresponder à cadeia de caracteres de formato.</span><span class="sxs-lookup"><span data-stu-id="48582-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="48582-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="48582-115">Example</span></span>

<span data-ttu-id="48582-116">Essa função imprime uma cadeia de caracteres para mostrar que o controle foi passado para ela.</span><span class="sxs-lookup"><span data-stu-id="48582-116">This function prints a string to show that control was passed to it.</span></span> <span data-ttu-id="48582-117">O sinalizador _DEBUG deve ser definido antes da compilação ou esta função não faz nada.</span><span class="sxs-lookup"><span data-stu-id="48582-117">The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a><span data-ttu-id="48582-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="48582-118">See also</span></span>



[<span data-ttu-id="48582-119">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="48582-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

