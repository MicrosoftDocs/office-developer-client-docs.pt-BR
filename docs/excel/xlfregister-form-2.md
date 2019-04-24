---
title: xlfRegister (Formulário 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- função xlfregister [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66af741456ab763ef346a8777429f0ae1be77c11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310119"
---
# <a name="xlfregister-form-2"></a><span data-ttu-id="1d334-104">xlfRegister (Formulário 2)</span><span class="sxs-lookup"><span data-stu-id="1d334-104">xlfRegister (Form 2)</span></span>

 <span data-ttu-id="1d334-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1d334-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1d334-106">Pode ser chamado de um comando DLL ou XLL que, por sua vez, foi chamado pelo Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="1d334-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="1d334-107">Isso equivale a chamar **Register** de uma folha de macro XLM do Excel.</span><span class="sxs-lookup"><span data-stu-id="1d334-107">This is equivalent to calling **REGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="1d334-108">A função **xlfRegister** pode ser chamada em duas formas:</span><span class="sxs-lookup"><span data-stu-id="1d334-108">The **xlfRegister** function can be called in two forms:</span></span> 
  
- <span data-ttu-id="1d334-109">[xlfRegister (formulário 1)](xlfregister-form-1.md): registra um comando ou função individual.</span><span class="sxs-lookup"><span data-stu-id="1d334-109">[xlfRegister (Form 1)](xlfregister-form-1.md): Registers an individual command or function.</span></span>
    
- <span data-ttu-id="1d334-110">xlfRegister (Formato 2): carrega e ativa um XLL.</span><span class="sxs-lookup"><span data-stu-id="1d334-110">xlfRegister (Form 2): Loads and activates an XLL.</span></span>
    
<span data-ttu-id="1d334-111">Chamado no formato 2, essa função só pode ser usada para carregar e ativar um XLL contendo um procedimento [xlAutoOpen](xlautoopen.md) .</span><span class="sxs-lookup"><span data-stu-id="1d334-111">Called in Form 2, this function can only be used to load and activate an XLL containing an [xlAutoOpen](xlautoopen.md) procedure.</span></span> 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="1d334-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d334-112">Parameters</span></span>

 <span data-ttu-id="1d334-113">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="1d334-113">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="1d334-114">O nome da DLL a ser carregada e ativada.</span><span class="sxs-lookup"><span data-stu-id="1d334-114">The name of the DLL to be loaded and activated.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="1d334-115">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1d334-115">Property value/Return value</span></span>

<span data-ttu-id="1d334-116">Se tiver êxito, retornará o nome da DLL (**xltypeStr**).</span><span class="sxs-lookup"><span data-stu-id="1d334-116">If successful, this returns the name of the DLL (**xltypeStr**).</span></span> <span data-ttu-id="1d334-117">Caso contrário, retornará um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="1d334-117">Otherwise it returns a #VALUE!</span></span> <span data-ttu-id="1d334-118">#NUM!</span><span class="sxs-lookup"><span data-stu-id="1d334-118">error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1d334-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d334-119">See also</span></span>



[<span data-ttu-id="1d334-120">Funções XLM essenciais e úteis para a API C</span><span class="sxs-lookup"><span data-stu-id="1d334-120">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

