---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- função xlAutoClose [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3cbe1cd879fb5a91d14b38f8a659a7f77d943fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765469"
---
# <a name="xlautoclose"></a><span data-ttu-id="8298f-104">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="8298f-104">xlAutoClose</span></span>

 <span data-ttu-id="8298f-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8298f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8298f-106">Chamado pelo Microsoft Excel sempre que o XLL é desativado.</span><span class="sxs-lookup"><span data-stu-id="8298f-106">Called by Microsoft Excel whenever the XLL is deactivated.</span></span> <span data-ttu-id="8298f-107">O suplemento é desativado quando uma sessão do Excel é encerrada normalmente.</span><span class="sxs-lookup"><span data-stu-id="8298f-107">The add-in is deactivated when an Excel session ends normally.</span></span> <span data-ttu-id="8298f-108">O suplemento pode ser desativado pelo usuário durante uma sessão do Excel e essa função será chamada nesse caso.</span><span class="sxs-lookup"><span data-stu-id="8298f-108">The add-in can be deactivated by the user during an Excel session, and this function will be called in that case.</span></span>
  
<span data-ttu-id="8298f-109">Excel não exige um XLL implementar e exportar essa função, apesar de ser recomendável para que seu XLL pode cancelar o registro de funções e comandos, liberar recursos, desfazer personalizações e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8298f-109">Excel does not require an XLL to implement and export this function, although it is advisable so that your XLL can unregister functions and commands, release resources, undo customizations, and so on.</span></span> <span data-ttu-id="8298f-110">Se as funções e comandos não são explicitamente não registrados pelo XLL, o Excel faz isso depois de chamar a função **xlAutoClose** .</span><span class="sxs-lookup"><span data-stu-id="8298f-110">If functions and commands are not explicitly unregistered by the XLL, Excel does this after calling the **xlAutoClose** function.</span></span> 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a><span data-ttu-id="8298f-111">Par�metros</span><span class="sxs-lookup"><span data-stu-id="8298f-111">Parameters</span></span>

<span data-ttu-id="8298f-112">Essa função não assume nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="8298f-112">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="8298f-113">Propriedade valor/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8298f-113">Property value/Return value</span></span>

<span data-ttu-id="8298f-114">A implementação dessa função deve retornar 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="8298f-114">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8298f-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="8298f-115">Remarks</span></span>

<span data-ttu-id="8298f-116">Excel chama a função **xlAutoClose** sempre que o XLL estiver desativado, ou seja, descarregado da memória.</span><span class="sxs-lookup"><span data-stu-id="8298f-116">Excel calls the **xlAutoClose** function whenever the XLL is deactivated, that is, unloaded from memory.</span></span> <span data-ttu-id="8298f-117">XLL é desativado nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="8298f-117">The XLL is deactivated in the following situations:</span></span> 
  
- <span data-ttu-id="8298f-118">No final de uma sessão do Excel se ativo durante a sessão normal.</span><span class="sxs-lookup"><span data-stu-id="8298f-118">At the normal end of an Excel session if active during that session.</span></span>
    
- <span data-ttu-id="8298f-119">Se explicitamente descarregado durante uma sessão do Excel.</span><span class="sxs-lookup"><span data-stu-id="8298f-119">If explicitly unloaded during an Excel session.</span></span>
    
- <span data-ttu-id="8298f-120">Um XLL pode ser descarregado de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="8298f-120">An XLL can be unloaded in several ways:</span></span>
    
- <span data-ttu-id="8298f-121">Usando o Gerenciador de suplemento.</span><span class="sxs-lookup"><span data-stu-id="8298f-121">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="8298f-122">A partir de outra XLL que chama [xlfUnregister](xlfunregister-form-1.md) com o nome dessa DLL como o único argumento.</span><span class="sxs-lookup"><span data-stu-id="8298f-122">From another XLL that calls [xlfUnregister](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="8298f-123">De uma folha de macro XLM que chama [cancela o registro](xlfunregister-form-1.md) com o nome dessa DLL como o único argumento.</span><span class="sxs-lookup"><span data-stu-id="8298f-123">From an XLM macro sheet that calls [UNREGISTER](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
<span data-ttu-id="8298f-124">Essa função deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8298f-124">This function should do the following:</span></span>
  
- <span data-ttu-id="8298f-125">Remova os menus ou itens de menu que foram adicionados pelo XLL.</span><span class="sxs-lookup"><span data-stu-id="8298f-125">Remove any menus or menu items that were added by the XLL.</span></span>
    
- <span data-ttu-id="8298f-126">Execute qualquer limpeza global necessária.</span><span class="sxs-lookup"><span data-stu-id="8298f-126">Perform any necessary global cleanup.</span></span>
    
- <span data-ttu-id="8298f-127">Exclua todos os nomes que foram criados, especialmente os nomes das funções exportadas.</span><span class="sxs-lookup"><span data-stu-id="8298f-127">Delete any names that were created, especially names of exported functions.</span></span> <span data-ttu-id="8298f-128">Lembre-se de que registrar funções pode causar alguns nomes a serem criados, se o quarto argumento para **registrar** estiver presente.</span><span class="sxs-lookup"><span data-stu-id="8298f-128">Remember that registering functions may cause some names to be created, if the fourth argument to **REGISTER** is present.</span></span> 
    
## <a name="example"></a><span data-ttu-id="8298f-129">Example</span><span class="sxs-lookup"><span data-stu-id="8298f-129">Example</span></span>

<span data-ttu-id="8298f-130">Consulte os arquivos `SAMPLES\EXAMPLE\EXAMPLE.C` e `SAMPLES\GENERIC\GENERIC.C` por exemplo implementações dessa função.</span><span class="sxs-lookup"><span data-stu-id="8298f-130">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="8298f-131">O código a seguir é de `SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="8298f-131">The following code is from  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
```cs
int WINAPI xlAutoClose(void)
{
   int i;
   XLOPER12 xRes;
//
// This block first deletes all names added by xlAutoOpen or
// xlAutoRegister12. Next, it checks if the drop-down menu Generic still
// exists. If it does, it is deleted using xlfDeleteMenu. It then checks
// if the Test toolbar still exists. If it is, xlfDeleteToolbar is
// used to delete it.
//
// The following code to delete the defined names
// does not work in the current version of Excel. 
// You cannot delete these names once they are Registered.
// The code is left here in case the functionality becomes 
// available in a future version.
//
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgWorksheetFuncs[i][2]));
   for (i = 0; i < g_rgCommandFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgCommandFuncs[i][2]));
//
// Everything else works as documented.
//
   Excel12f(xlfGetBar, &amp;xRes, 3, TempInt12(10), TempStr12(L"Generic"), TempInt12(0));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteMenu, 0, 2, TempNum12(10), TempStr12(L"Generic"));
      // Free the XLOPER12 returned by xlfGetBar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   Excel12f(xlfGetToolbar, &amp;xRes, 2, TempInt12(7), TempStr12(L"Test"));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteToolbar, 0, 1, TempStr12(L"Test"));
      // Free the XLOPER12 returned by xlfGetToolbar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="8298f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="8298f-132">See also</span></span>



[<span data-ttu-id="8298f-133">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="8298f-133">xlAutoOpen</span></span>](xlautoopen.md)


[<span data-ttu-id="8298f-134">Gerenciador de suplemento e funções da Interface XLL</span><span class="sxs-lookup"><span data-stu-id="8298f-134">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

