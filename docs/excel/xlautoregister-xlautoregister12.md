---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- função xlAutoRegister [Excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303945"
---
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="b61c7-104">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="b61c7-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="b61c7-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b61c7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b61c7-106">O Excel chama a [função xlAutoRegister](xlautoregister-xlautoregister12.md) sempre que uma chamada foi feita ao registrador \*\*\*\* de função XLM ou à [função xlfRegister](xlfregister-form-1.md)equivalente da API C, com os tipos de argumento e de retorno da função que está sendo registrada ausente.</span><span class="sxs-lookup"><span data-stu-id="b61c7-106">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing.</span></span> <span data-ttu-id="b61c7-107">Permite que o XLL pesquise suas listas internas de funções e comandos exportados para registrar a função com os tipos de argumento e de retorno especificados.</span><span class="sxs-lookup"><span data-stu-id="b61c7-107">It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="b61c7-108">A partir do Excel 2007, o Excel chama a função **xlAutoRegister12** em preferência para a função **xlAutoRegister** se ela for exportada pelo XLL.</span><span class="sxs-lookup"><span data-stu-id="b61c7-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="b61c7-109">O Excel não requer que um XLL implemente e exporte uma dessas funções.</span><span class="sxs-lookup"><span data-stu-id="b61c7-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b61c7-110">Se **xlAutoRegister**/ **xlAutoRegister12** tentar registrar a função sem fornecer os tipos de argumento e de retorno, ocorrerá um loop de chamada recursiva, que eventualmente estourará a pilha de chamadas e travará o Excel.</span><span class="sxs-lookup"><span data-stu-id="b61c7-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="b61c7-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b61c7-111">Parameters</span></span>

 <span data-ttu-id="b61c7-112">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="b61c7-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="b61c7-113">O nome da função XLL que está sendo registrada.</span><span class="sxs-lookup"><span data-stu-id="b61c7-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b61c7-114">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b61c7-114">Property value/Return value</span></span>

<span data-ttu-id="b61c7-115">A função deve retornar o resultado da tentativa de registrar a função XLL _pxName_ usando a função **xlfRegister** .</span><span class="sxs-lookup"><span data-stu-id="b61c7-115">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function.</span></span> <span data-ttu-id="b61c7-116">Se a função especificada não for uma das exportações do XLL, ela deverá retornar o **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="b61c7-116">If the specified function is not one of the XLL's exports, it should return the **#VALUE!**</span></span> <span data-ttu-id="b61c7-117">erro ou **nulo** que o Excel irá interpretar em **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="b61c7-117">error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b61c7-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b61c7-118">Remarks</span></span>

<span data-ttu-id="b61c7-119">Sua implementação do **xlAutoRegister** deve realizar uma pesquisa que não diferencia maiúsculas de minúsculas nas listas internas de funções e comandos que ele exporta procurando por uma correspondência com o nome aprovado.</span><span class="sxs-lookup"><span data-stu-id="b61c7-119">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name.</span></span> <span data-ttu-id="b61c7-120">Se a função ou o comando for encontrado, **xlAutoRegister** deve tentar registrá-lo, usando a função **xlfRegister** , certificando-se de fornecer a cadeia de caracteres que informa ao Excel os tipos de argumento e de retorno da função, bem como qualquer outro necessário informações sobre a função.</span><span class="sxs-lookup"><span data-stu-id="b61c7-120">If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function.</span></span> <span data-ttu-id="b61c7-121">Em seguida, ele deve retornar ao Excel, qualquer que seja a chamada para **xlfRegister** retornada.</span><span class="sxs-lookup"><span data-stu-id="b61c7-121">It should then return to Excel whatever the call to **xlfRegister** returned.</span></span> <span data-ttu-id="b61c7-122">Se a função foi registrada com êxito, **xlfRegister** retorna um valor **xltypeNum** que contém a ID de registro da função.</span><span class="sxs-lookup"><span data-stu-id="b61c7-122">If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="b61c7-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b61c7-123">Example</span></span>

<span data-ttu-id="b61c7-124">ConFira o `SAMPLES\EXAMPLE\EXAMPLE.C` arquivo para obter um exemplo de implementação dessa função.</span><span class="sxs-lookup"><span data-stu-id="b61c7-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b61c7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b61c7-125">See also</span></span>



[<span data-ttu-id="b61c7-126">REMOVER</span><span class="sxs-lookup"><span data-stu-id="b61c7-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="b61c7-127">UNREGISTER</span><span class="sxs-lookup"><span data-stu-id="b61c7-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

