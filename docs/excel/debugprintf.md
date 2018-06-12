---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- função debugprintf [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 25669cfc705e797b80be0fab590d809e8f1e3b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765261"
---
# <a name="debugprintf"></a><span data-ttu-id="d48d7-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="d48d7-104">debugPrintf</span></span>

<span data-ttu-id="d48d7-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d48d7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d48d7-106">Função da biblioteca Framework que grava uma sequência de byte terminada em nulo ao depurador ativo por meio da função **OutputDebugStringA**do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="d48d7-106">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**.</span></span> <span data-ttu-id="d48d7-107">Se o aplicativo não possui nenhum depurador, o depurador do sistema exibe a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d48d7-107">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="d48d7-108">Se o aplicativo não tem nenhum depurador e o depurador do sistema não está ativo, **debugPrintf** não fará nada.</span><span class="sxs-lookup"><span data-stu-id="d48d7-108">If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="d48d7-109">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d48d7-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="d48d7-110">Par�metros</span><span class="sxs-lookup"><span data-stu-id="d48d7-110">Parameters</span></span>

 <span data-ttu-id="d48d7-111">_lpFormat (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="d48d7-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="d48d7-112">A sequência de formato, que segue a sintaxe e as regras para que usados com a função **sprintf** .</span><span class="sxs-lookup"><span data-stu-id="d48d7-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="d48d7-113">_argumentos_</span><span class="sxs-lookup"><span data-stu-id="d48d7-113">_arguments_</span></span>
  
<span data-ttu-id="d48d7-114">Zero ou mais argumentos para coincidir com a cadeia de caracteres de formato.</span><span class="sxs-lookup"><span data-stu-id="d48d7-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="d48d7-115">Example</span><span class="sxs-lookup"><span data-stu-id="d48d7-115">Example</span></span>

<span data-ttu-id="d48d7-116">Essa função imprime uma cadeia de caracteres para mostrar que o controle foi passado para ele.</span><span class="sxs-lookup"><span data-stu-id="d48d7-116">This function prints a string to show that control was passed to it.</span></span> <span data-ttu-id="d48d7-117">O sinalizador _DEBUG deve ser definido antes de compilar senão essa função não faz nada.</span><span class="sxs-lookup"><span data-stu-id="d48d7-117">The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="d48d7-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d48d7-118">See also</span></span>



[<span data-ttu-id="d48d7-119">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="d48d7-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

