---
title: fDialog/fDialog12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- função fdialog [excel 2007],função fDialog12 [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58d0df500c38534ec1315d2dab1517c1f5272ad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431523"
---
# <a name="fdialogfdialog12"></a><span data-ttu-id="bc445-104">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="bc445-104">fDialog/fDialog12</span></span>

 <span data-ttu-id="bc445-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bc445-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bc445-106">Exemplo de comando definido pelo usuário que demonstra como criar uma UDD do Microsoft Excel (caixa de diálogo definida pelo usuário) em uma DLL usando os recursos da caixa de diálogo na API de C.</span><span class="sxs-lookup"><span data-stu-id="bc445-106">Example user-defined command that demonstrates how to create a Microsoft Excel UDD (user-defined dialog box) within a DLL by using the dialog box capabilities in the C API.</span></span> <span data-ttu-id="bc445-107">Quando GENERIC.xll é carregado, ele cria um menu definido pelo usuário, Genérico, por meio do qual esse comando é acessado.</span><span class="sxs-lookup"><span data-stu-id="bc445-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="bc445-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc445-108">Parameters</span></span>

<span data-ttu-id="bc445-109">A função não aceita parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bc445-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="bc445-110">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bc445-110">Property value/Return value</span></span>

<span data-ttu-id="bc445-111">A função sempre retorna 1.</span><span class="sxs-lookup"><span data-stu-id="bc445-111">The function always returns 1.</span></span>
  
### <a name="example"></a><span data-ttu-id="bc445-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bc445-112">Example</span></span>

<span data-ttu-id="bc445-113">Consulte  `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para esta função.</span><span class="sxs-lookup"><span data-stu-id="bc445-113">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc445-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc445-114">See also</span></span>



[<span data-ttu-id="bc445-115">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="bc445-115">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

