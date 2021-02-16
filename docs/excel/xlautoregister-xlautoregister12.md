---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- Função xlautoregister [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421162"
---
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="d06be-104">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="d06be-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="d06be-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d06be-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d06be-106">O Excel chama a função [xlAutoRegister](xlautoregister-xlautoregister12.md) sempre que uma chamada é feita para a função XLM **REGISTER** ou a função [equivalente xlfRegister](xlfregister-form-1.md)da API C, com os tipos de retorno e argumento da função sendo registrada ausentes.</span><span class="sxs-lookup"><span data-stu-id="d06be-106">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing.</span></span> <span data-ttu-id="d06be-107">Ele permite que o XLL pesquise suas listas internas de funções e comandos exportados para registrar a função com o argumento e os tipos de retorno especificados.</span><span class="sxs-lookup"><span data-stu-id="d06be-107">It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="d06be-108">A partir do Excel 2007, o Excel chama a função **xlAutoRegister12** de preferência para a função **xlAutoRegister** se ela for exportada pelo XLL.</span><span class="sxs-lookup"><span data-stu-id="d06be-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="d06be-109">O Excel não exige um XLL para implementar e exportar qualquer uma dessas funções.</span><span class="sxs-lookup"><span data-stu-id="d06be-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d06be-110">Se **xlAutoRegister** /  **xlAutoRegister12** tentar registrar a função sem fornecer o argumento e os tipos de retorno, ocorrerá um loop de chamada recursiva que eventualmente exceda a pilha de chamada e trava o Excel.</span><span class="sxs-lookup"><span data-stu-id="d06be-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="d06be-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d06be-111">Parameters</span></span>

 <span data-ttu-id="d06be-112">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="d06be-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="d06be-113">O nome da função XLL que está sendo registrada.</span><span class="sxs-lookup"><span data-stu-id="d06be-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d06be-114">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d06be-114">Property value/Return value</span></span>

<span data-ttu-id="d06be-115">A função deve retornar o resultado da tentativa de registrar a função _PXName_ XLL usando a **função xlfRegister.**</span><span class="sxs-lookup"><span data-stu-id="d06be-115">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function.</span></span> <span data-ttu-id="d06be-116">Se a função especificada não for uma das exportações do XLL, ela deverá retornar o **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="d06be-116">If the specified function is not one of the XLL's exports, it should return the **#VALUE!**</span></span> <span data-ttu-id="d06be-117">ou **NULL** que o Excel interpretará em **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="d06be-117">error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d06be-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d06be-118">Remarks</span></span>

<span data-ttu-id="d06be-119">Sua implementação do **xlAutoRegister** deve realizar uma pesquisa que não faça maiúsculas de minúsculas nas listas internas de funções e comandos do XLL que ele exporta procurando uma combinação com o nome passado.</span><span class="sxs-lookup"><span data-stu-id="d06be-119">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name.</span></span> <span data-ttu-id="d06be-120">Se a função ou o comando for encontrado, **xlAutoRegister** deverá tentar registrá-lo, usando a função **xlfRegister,** fornecendo a cadeia de caracteres que informa ao Excel os tipos de retorno e argumento da função, bem como quaisquer outras informações necessárias sobre a função.</span><span class="sxs-lookup"><span data-stu-id="d06be-120">If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function.</span></span> <span data-ttu-id="d06be-121">Em seguida, ele deve retornar ao Excel independentemente da chamada para **xlfRegister** retornada.</span><span class="sxs-lookup"><span data-stu-id="d06be-121">It should then return to Excel whatever the call to **xlfRegister** returned.</span></span> <span data-ttu-id="d06be-122">Se a função tiver sido registrada com êxito, **xlfRegister** retornará um valor **xltypeNum** contendo a ID do Registro da função.</span><span class="sxs-lookup"><span data-stu-id="d06be-122">If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="d06be-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d06be-123">Example</span></span>

<span data-ttu-id="d06be-124">Consulte o arquivo  `SAMPLES\EXAMPLE\EXAMPLE.C` para ver um exemplo de implementação dessa função.</span><span class="sxs-lookup"><span data-stu-id="d06be-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d06be-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d06be-125">See also</span></span>



[<span data-ttu-id="d06be-126">REGISTER</span><span class="sxs-lookup"><span data-stu-id="d06be-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="d06be-127">UNREGISTER</span><span class="sxs-lookup"><span data-stu-id="d06be-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

