---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- função fexit [Excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310854"
---
# <a name="fexit"></a><span data-ttu-id="5fc36-104">fExit</span><span class="sxs-lookup"><span data-stu-id="5fc36-104">fExit</span></span>

 <span data-ttu-id="5fc36-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5fc36-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5fc36-106">Exemplo de comando definido pelo usuário que descarrega GENERIC. XLL.</span><span class="sxs-lookup"><span data-stu-id="5fc36-106">Example user-defined command that unloads GENERIC.xll.</span></span> <span data-ttu-id="5fc36-107">Quando GENERIC. XLL é carregado, ele cria um menu definido pelo usuário, genérico, através do qual este comando é acessado.</span><span class="sxs-lookup"><span data-stu-id="5fc36-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span> 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a><span data-ttu-id="5fc36-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fc36-108">Parameters</span></span>

<span data-ttu-id="5fc36-109">A função não utiliza parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5fc36-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="5fc36-110">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5fc36-110">Property value/Return value</span></span>

<span data-ttu-id="5fc36-111">A função sempre retorna 1.</span><span class="sxs-lookup"><span data-stu-id="5fc36-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5fc36-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fc36-112">Remarks</span></span>

<span data-ttu-id="5fc36-113">Esta é uma rotina iniciada pelo usuário para sair genérica. XLL você deve evitar simplesmente `UNREGISTER("GENERIC.XLL")` chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="5fc36-113">This is a user-initiated routine to exit GENERIC.xll You should avoid simply calling  `UNREGISTER("GENERIC.XLL")` in this function.</span></span> <span data-ttu-id="5fc36-114">Isso forçaria a cancelar o registro de todas as funções nessa DLL, mesmo que elas estejam registradas em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="5fc36-114">This would forcefully unregister all the functions in this DLL, even if they are registered somewhere else.</span></span> <span data-ttu-id="5fc36-115">Em vez disso, cancele o registro de funções, uma de cada vez.</span><span class="sxs-lookup"><span data-stu-id="5fc36-115">Instead, unregister the functions one at a time.</span></span> 
  
### <a name="example"></a><span data-ttu-id="5fc36-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5fc36-116">Example</span></span>

<span data-ttu-id="5fc36-117">Consulte `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="5fc36-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5fc36-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fc36-118">See also</span></span>



[<span data-ttu-id="5fc36-119">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="5fc36-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

