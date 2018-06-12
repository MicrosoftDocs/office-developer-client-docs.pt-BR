---
title: xlfRegister (formulário 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- função xlfRegister [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a535018e2b644966d183ba9ae862ce83670c9231
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765465"
---
# <a name="xlfregister-form-2"></a><span data-ttu-id="41ad8-104">xlfRegister (formulário 2)</span><span class="sxs-lookup"><span data-stu-id="41ad8-104">xlfRegister (Form 2)</span></span>

 <span data-ttu-id="41ad8-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="41ad8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="41ad8-106">Pode ser chamado a partir de um comando DLL ou XLL próprio foi chamado pelo Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="41ad8-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="41ad8-107">Isso é equivalente a chamar **registrar** a partir de uma folha de macro do Excel XLM.</span><span class="sxs-lookup"><span data-stu-id="41ad8-107">This is equivalent to calling **REGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="41ad8-108">A função **xlfRegister** pode ser chamada de duas formas:</span><span class="sxs-lookup"><span data-stu-id="41ad8-108">The **xlfRegister** function can be called in two forms:</span></span> 
  
- <span data-ttu-id="41ad8-109">[xlfRegister (formulário 1)](xlfregister-form-1.md): registra um comando individual ou uma função.</span><span class="sxs-lookup"><span data-stu-id="41ad8-109">[xlfRegister (Form 1)](xlfregister-form-1.md): Registers an individual command or function.</span></span>
    
- <span data-ttu-id="41ad8-110">xlfRegister (formulário 2): cargas e ativa um XLL.</span><span class="sxs-lookup"><span data-stu-id="41ad8-110">xlfRegister (Form 2): Loads and activates an XLL.</span></span>
    
<span data-ttu-id="41ad8-111">Chamado no formulário 2, essa função pode ser usada apenas para carregar e ativar um XLL contendo um procedimento [xlAutoOpen](xlautoopen.md) .</span><span class="sxs-lookup"><span data-stu-id="41ad8-111">Called in Form 2, this function can only be used to load and activate an XLL containing an [xlAutoOpen](xlautoopen.md) procedure.</span></span> 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="41ad8-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="41ad8-112">Parameters</span></span>

 <span data-ttu-id="41ad8-113">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="41ad8-113">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="41ad8-114">O nome da DLL seja carregado e ativado.</span><span class="sxs-lookup"><span data-stu-id="41ad8-114">The name of the DLL to be loaded and activated.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="41ad8-115">Propriedade valor/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="41ad8-115">Property value/Return value</span></span>

<span data-ttu-id="41ad8-116">Se tiver êxito, isso retorna o nome da DLL (**xltypeStr**).</span><span class="sxs-lookup"><span data-stu-id="41ad8-116">If successful, this returns the name of the DLL (**xltypeStr**).</span></span> <span data-ttu-id="41ad8-117">Caso contrário, ele retornará um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="41ad8-117">Otherwise it returns a #VALUE!</span></span> <span data-ttu-id="41ad8-118">erro.</span><span class="sxs-lookup"><span data-stu-id="41ad8-118">error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="41ad8-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="41ad8-119">See also</span></span>



[<span data-ttu-id="41ad8-120">Funções de XLM API C essenciais e úteis</span><span class="sxs-lookup"><span data-stu-id="41ad8-120">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

