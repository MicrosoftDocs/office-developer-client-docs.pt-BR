---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- função fshowdialog [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6122e4b99c69cd1bd878c9267ff85f59d0f61998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433588"
---
# <a name="fshowdialog"></a><span data-ttu-id="3ff11-104">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="3ff11-104">fShowDialog</span></span>

 <span data-ttu-id="3ff11-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3ff11-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3ff11-106">Exemplo de comando definido pelo usuário que carrega e exibe um exemplo de caixa de diálogo nativa do Windows.</span><span class="sxs-lookup"><span data-stu-id="3ff11-106">Example user-defined command that loads and displays an example native Windows dialog box.</span></span> <span data-ttu-id="3ff11-107">Quando GENERIC.xll é carregado, ele cria um menu definido pelo usuário, Genérico, por meio do qual esse comando é acessado.</span><span class="sxs-lookup"><span data-stu-id="3ff11-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="3ff11-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ff11-108">Parameters</span></span>

<span data-ttu-id="3ff11-109">A função não aceita parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3ff11-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="3ff11-110">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3ff11-110">Property value/Return value</span></span>

<span data-ttu-id="3ff11-111">A função retorna o número inteiro zero para indicar a conclusão bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="3ff11-111">The function return integer zero to indicate successful completion</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3ff11-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ff11-112">Remarks</span></span>

<span data-ttu-id="3ff11-113">As etapas para exibir a caixa de diálogo nativa do Windows são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="3ff11-113">The steps to display the native Windows dialog box are as follows:</span></span>
  
1. <span data-ttu-id="3ff11-114">Obtenha o alça principal do Windows do Microsoft Excel usando **GetHwnd**.</span><span class="sxs-lookup"><span data-stu-id="3ff11-114">Obtain the Microsoft Excel main Windows handle using **GetHwnd**.</span></span>
    
2. <span data-ttu-id="3ff11-115">Conectar a janela principal do Excel **usando HookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="3ff11-115">Hook the Excel main window using **HookExcelWindow**.</span></span>
    
3. <span data-ttu-id="3ff11-116">Exibir a caixa de diálogo usando **DialogBox**.</span><span class="sxs-lookup"><span data-stu-id="3ff11-116">Display the dialog box using **DialogBox**.</span></span>
    
4. <span data-ttu-id="3ff11-117">Desaconsinchar a janela principal do Excel **usando UnhookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="3ff11-117">Unhook the Excel main window using **UnhookExcelWindow**.</span></span>
    
### <a name="example"></a><span data-ttu-id="3ff11-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3ff11-118">Example</span></span>

<span data-ttu-id="3ff11-119">Consulte  `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para esta função.</span><span class="sxs-lookup"><span data-stu-id="3ff11-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ff11-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ff11-120">See also</span></span>



[<span data-ttu-id="3ff11-121">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="3ff11-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

