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
- função fdialog [excel 2007], função fDialog12 [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 554b76d2d316110286e83158acfff33aa68e19c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765367"
---
# <a name="fdialogfdialog12"></a><span data-ttu-id="41075-104">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="41075-104">fDialog/fDialog12</span></span>

 <span data-ttu-id="41075-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="41075-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="41075-106">Definido pelo usuário comando de exemplo que demonstra como criar um UDD de Excel da Microsoft (caixa de diálogo definidas pelo usuário) dentro de uma DLL usando os recursos de caixa de diálogo do C API.</span><span class="sxs-lookup"><span data-stu-id="41075-106">Example user-defined command that demonstrates how to create a Microsoft Excel UDD (user-defined dialog box) within a DLL by using the dialog box capabilities in the C API.</span></span> <span data-ttu-id="41075-107">Quando GENERIC.xll é carregado, ele cria um menu definidas pelo usuário, genérico, através do qual esse comando é acessado.</span><span class="sxs-lookup"><span data-stu-id="41075-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="41075-108">Par�metros</span><span class="sxs-lookup"><span data-stu-id="41075-108">Parameters</span></span>

<span data-ttu-id="41075-109">A função não assumir nenhum parâmetro.</span><span class="sxs-lookup"><span data-stu-id="41075-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="41075-110">Propriedade valor/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="41075-110">Property value/Return value</span></span>

<span data-ttu-id="41075-111">A função sempre retornará 1.</span><span class="sxs-lookup"><span data-stu-id="41075-111">The function always returns 1.</span></span>
  
### <a name="example"></a><span data-ttu-id="41075-112">Example</span><span class="sxs-lookup"><span data-stu-id="41075-112">Example</span></span>

<span data-ttu-id="41075-113">Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="41075-113">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="41075-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="41075-114">See also</span></span>



[<span data-ttu-id="41075-115">Funções na DLL genérico</span><span class="sxs-lookup"><span data-stu-id="41075-115">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

