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
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ae6d8b2f0b95641678947e9bd75daa2237b080b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765381"
---
# <a name="fshowdialog"></a><span data-ttu-id="39f88-104">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="39f88-104">fShowDialog</span></span>

 <span data-ttu-id="39f88-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="39f88-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="39f88-106">Definido pelo usuário comando de exemplo que carrega e exibe uma caixa de diálogo de Windows nativa do exemplo.</span><span class="sxs-lookup"><span data-stu-id="39f88-106">Example user-defined command that loads and displays an example native Windows dialog box.</span></span> <span data-ttu-id="39f88-107">Quando GENERIC.xll é carregado, ele cria um menu definidas pelo usuário, genérico, através do qual esse comando é acessado.</span><span class="sxs-lookup"><span data-stu-id="39f88-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="39f88-108">Par�metros</span><span class="sxs-lookup"><span data-stu-id="39f88-108">Parameters</span></span>

<span data-ttu-id="39f88-109">A função não assumir nenhum parâmetro.</span><span class="sxs-lookup"><span data-stu-id="39f88-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="39f88-110">Propriedade valor/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="39f88-110">Property value/Return value</span></span>

<span data-ttu-id="39f88-111">O inteiro de retorno de função zero para indicar a conclusão bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="39f88-111">The function return integer zero to indicate successful completion</span></span>
  
## <a name="remarks"></a><span data-ttu-id="39f88-112">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="39f88-112">Remarks</span></span>

<span data-ttu-id="39f88-113">As etapas para exibir a caixa de diálogo nativa do Windows são da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="39f88-113">The steps to display the native Windows dialog box are as follows:</span></span>
  
1. <span data-ttu-id="39f88-114">Obter o identificador de Windows principal do Microsoft Excel usando **GetHwnd**.</span><span class="sxs-lookup"><span data-stu-id="39f88-114">Obtain the Microsoft Excel main Windows handle using **GetHwnd**.</span></span>
    
2. <span data-ttu-id="39f88-115">Capturar a janela principal do Excel usando **HookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="39f88-115">Hook the Excel main window using **HookExcelWindow**.</span></span>
    
3. <span data-ttu-id="39f88-116">Exibe a caixa de diálogo usando **DialogBox**.</span><span class="sxs-lookup"><span data-stu-id="39f88-116">Display the dialog box using **DialogBox**.</span></span>
    
4. <span data-ttu-id="39f88-117">Solte a janela principal do Excel usando **UnhookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="39f88-117">Unhook the Excel main window using **UnhookExcelWindow**.</span></span>
    
### <a name="example"></a><span data-ttu-id="39f88-118">Example</span><span class="sxs-lookup"><span data-stu-id="39f88-118">Example</span></span>

<span data-ttu-id="39f88-119">Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="39f88-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="39f88-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="39f88-120">See also</span></span>



[<span data-ttu-id="39f88-121">Funções na DLL genérico</span><span class="sxs-lookup"><span data-stu-id="39f88-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

