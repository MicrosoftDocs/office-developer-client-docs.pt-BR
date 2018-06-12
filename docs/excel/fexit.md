---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- função fexit [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3abb5cd68a45fbcd16665dbc4d492d764bbd315e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765362"
---
# <a name="fexit"></a><span data-ttu-id="9734f-104">fExit</span><span class="sxs-lookup"><span data-stu-id="9734f-104">fExit</span></span>

 <span data-ttu-id="9734f-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9734f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9734f-106">Definido pelo usuário comando de exemplo que descarrega GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="9734f-106">Example user-defined command that unloads GENERIC.xll.</span></span> <span data-ttu-id="9734f-107">Quando GENERIC.xll é carregado, ele cria um menu definidas pelo usuário, genérico, através do qual esse comando é acessado.</span><span class="sxs-lookup"><span data-stu-id="9734f-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span> 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a><span data-ttu-id="9734f-108">Par�metros</span><span class="sxs-lookup"><span data-stu-id="9734f-108">Parameters</span></span>

<span data-ttu-id="9734f-109">A função não assumir nenhum parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9734f-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9734f-110">Propriedade valor/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9734f-110">Property value/Return value</span></span>

<span data-ttu-id="9734f-111">A função sempre retornará 1.</span><span class="sxs-lookup"><span data-stu-id="9734f-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9734f-112">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="9734f-112">Remarks</span></span>

<span data-ttu-id="9734f-113">Isso é uma rotina iniciadas pelo usuário para sair GENERIC.xll Evite simplesmente chamar `UNREGISTER("GENERIC.XLL")` nessa função.</span><span class="sxs-lookup"><span data-stu-id="9734f-113">This is a user-initiated routine to exit GENERIC.xll You should avoid simply calling  `UNREGISTER("GENERIC.XLL")` in this function.</span></span> <span data-ttu-id="9734f-114">Isso seria forçada cancelar o registro de todas as funções nessa DLL, mesmo se eles são registrados em algum lugar else.</span><span class="sxs-lookup"><span data-stu-id="9734f-114">This would forcefully unregister all the functions in this DLL, even if they are registered somewhere else.</span></span> <span data-ttu-id="9734f-115">Cancelar o registro em vez disso, as funções de um por vez.</span><span class="sxs-lookup"><span data-stu-id="9734f-115">Instead, unregister the functions one at a time.</span></span> 
  
### <a name="example"></a><span data-ttu-id="9734f-116">Example</span><span class="sxs-lookup"><span data-stu-id="9734f-116">Example</span></span>

<span data-ttu-id="9734f-117">Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="9734f-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9734f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="9734f-118">See also</span></span>



[<span data-ttu-id="9734f-119">Funções na DLL genérico</span><span class="sxs-lookup"><span data-stu-id="9734f-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

