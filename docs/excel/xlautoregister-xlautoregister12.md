---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- função xlautoregister [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6430a54b0c0ed3b6e08d3c9256cae7dcde926ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19765453"
---
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="4c8e8-104">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="4c8e8-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="4c8e8-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4c8e8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4c8e8-106">Excel chama a [função xlAutoRegister](xlautoregister-xlautoregister12.md) sempre que uma chamada foi feita para a função XLM **registrar**ou C API equivalente [xlfRegister função](xlfregister-form-1.md), com os tipos de retorno e o argumento da função que está sendo registrado ausente.</span><span class="sxs-lookup"><span data-stu-id="4c8e8-106">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing.</span></span> <span data-ttu-id="4c8e8-107">Ele permite que o XLL pesquisar seus listas internas de funções exportadas e comandos para registrar a função com o argumento e retornar tipos especificados.</span><span class="sxs-lookup"><span data-stu-id="4c8e8-107">It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="4c8e8-108">Iniciando no Excel 2007, Excel chama a função **xlAutoRegister12** em preferência a função **xlAutoRegister** se ele é exportado pelo XLL.</span><span class="sxs-lookup"><span data-stu-id="4c8e8-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="4c8e8-109">Excel não exige um XLL implementar e exportar qualquer uma dessas funções.</span><span class="sxs-lookup"><span data-stu-id="4c8e8-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4c8e8-110">Se **xlAutoRegister**/ **xlAutoRegister12** tenta registrar a função sem fornecer o argumento e tipos de retorno, um loop de chamada recursiva ocorre que eventualmente estourar a pilha de chamada e Excel de travamento.</span><span class="sxs-lookup"><span data-stu-id="4c8e8-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="4c8e8-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c8e8-111">Parameters</span></span>

 <span data-ttu-id="4c8e8-112">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="4c8e8-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="4c8e8-113">O nome da função XLL que está sendo registrado.</span><span class="sxs-lookup"><span data-stu-id="4c8e8-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="4c8e8-114">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4c8e8-114">Property value/Return value</span></span>

<span data-ttu-id="4c8e8-115">A função deve retornar o resultado da tentativa de registrar a função XLL _pxName_ , usando a função **xlfRegister** .</span><span class="sxs-lookup"><span data-stu-id="4c8e8-115">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function.</span></span> <span data-ttu-id="4c8e8-116">Se a função especificada não for uma das exportações do XLL, ele deve retornar o **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="4c8e8-116">If the specified function is not one of the XLL's exports, it should return the **#VALUE!**</span></span> <span data-ttu-id="4c8e8-117">erro ou **Nulo** que Excel irá interpretar em **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="4c8e8-117">error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c8e8-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c8e8-118">Remarks</span></span>

<span data-ttu-id="4c8e8-119">A implementação dos **xlAutoRegister** deve realizar uma pesquisa diferenciam maiusculas e minúsculas através de listas de interno do seu XLL das funções e comandos que ele exporta procurando uma correspondência com o nome passado.</span><span class="sxs-lookup"><span data-stu-id="4c8e8-119">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name.</span></span> <span data-ttu-id="4c8e8-120">Se a função ou o comando for localizado, **xlAutoRegister** deve tentar registrar a ele, usando a função **xlfRegister** , certificando-se de fornecer a cadeia de caracteres que indica os tipos de retorno e o argumento de função, bem como qualquer outro necessários ao Excel informações sobre a função.</span><span class="sxs-lookup"><span data-stu-id="4c8e8-120">If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function.</span></span> <span data-ttu-id="4c8e8-121">Em seguida, ele deverá retornar para o Excel vivo do que a chamada para **xlfRegister** retornado.</span><span class="sxs-lookup"><span data-stu-id="4c8e8-121">It should then return to Excel whatever the call to **xlfRegister** returned.</span></span> <span data-ttu-id="4c8e8-122">Se a função foi registrada com êxito, **xlfRegister** retorna um valor **xltypeNum** que contém a ID de registrar da função.</span><span class="sxs-lookup"><span data-stu-id="4c8e8-122">If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="4c8e8-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4c8e8-123">Example</span></span>

<span data-ttu-id="4c8e8-124">Consulte o arquivo `SAMPLES\EXAMPLE\EXAMPLE.C` para um exemplo de implementação dessa função.</span><span class="sxs-lookup"><span data-stu-id="4c8e8-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4c8e8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c8e8-125">See also</span></span>



[<span data-ttu-id="4c8e8-126">REGISTRAR</span><span class="sxs-lookup"><span data-stu-id="4c8e8-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="4c8e8-127">CANCELAR O REGISTRO</span><span class="sxs-lookup"><span data-stu-id="4c8e8-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

