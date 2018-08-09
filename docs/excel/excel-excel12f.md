---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- função do Excel [excel 2007], função Excel12f [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 56034984852713496465c3d1f79a9989fc47df1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765301"
---
# <a name="excelexcel12f"></a><span data-ttu-id="d0484-104">Excel/Excel12f</span><span class="sxs-lookup"><span data-stu-id="d0484-104">Excel/Excel12f</span></span>

 <span data-ttu-id="d0484-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d0484-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d0484-106">Funções da biblioteca de estrutura.</span><span class="sxs-lookup"><span data-stu-id="d0484-106">Framework library functions.</span></span> <span data-ttu-id="d0484-107">**Excel** é um wrapper para a função [Excel4](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="d0484-107">**Excel** is a wrapper for the [Excel4](excel4-excel12.md) function.</span></span> <span data-ttu-id="d0484-108">**Excel12f** é um wrapper para a função [Excel12](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="d0484-108">**Excel12f** is a wrapper for the [Excel12](excel4-excel12.md) function.</span></span> <span data-ttu-id="d0484-109">Cada verifica se nenhum dos argumentos é zero, o que indicaria que a criação de um temporário **XLOPER** ou **XLOPER12** falhou.</span><span class="sxs-lookup"><span data-stu-id="d0484-109">Each checks to see that none of the arguments is zero, which would indicate that the creation of a temporary **XLOPER** or **XLOPER12** failed.</span></span> <span data-ttu-id="d0484-110">Se ocorrer um erro, cada imprime uma mensagem de depuração.</span><span class="sxs-lookup"><span data-stu-id="d0484-110">If an error occurs, each prints a debug message.</span></span> <span data-ttu-id="d0484-111">Quando terminar, cada libera toda a memória temporária que possa ter sido criada para s temporário do **XLOPER**e **XLOPER12**s.</span><span class="sxs-lookup"><span data-stu-id="d0484-111">When finished, each frees all temporary memory that might have been created for temporary **XLOPER**s and **XLOPER12**s.</span></span>
  
 <span data-ttu-id="d0484-112">**Excel12f** só pode ser chamado a partir de uma DLL começando com a biblioteca do C API do Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="d0484-112">**Excel12f** can only be called from a DLL starting with the Excel 2007 C API library.</span></span> <span data-ttu-id="d0484-113">Além disso, ele só funciona durante a execução começando com o Excel 2007 e falha com **xlretFailed** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="d0484-113">Furthermore, it only works when running starting with Excel 2007, and fails with **xlretFailed** otherwise.</span></span> 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a><span data-ttu-id="d0484-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0484-114">Parameters</span></span>

 <span data-ttu-id="d0484-115">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="d0484-115">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="d0484-116">Um número indicando o comando ou uma função que você deseja chamar.</span><span class="sxs-lookup"><span data-stu-id="d0484-116">A number indicating the command or function you want to call.</span></span> <span data-ttu-id="d0484-117">Para obter mais informações, consulte [Excel4/Excel12](excel4-excel12.md).</span><span class="sxs-lookup"><span data-stu-id="d0484-117">For more information, see [Excel4/Excel12](excel4-excel12.md).</span></span>
  
 <span data-ttu-id="d0484-118">_pxRes_</span><span class="sxs-lookup"><span data-stu-id="d0484-118">_pxRes_</span></span>
  
<span data-ttu-id="d0484-119">Um ponteiro para o resultado da função avaliado.</span><span class="sxs-lookup"><span data-stu-id="d0484-119">A pointer to result of the evaluated function.</span></span> <span data-ttu-id="d0484-120">Qualquer memória apontada no resultado terá sido alocada pelo Excel e deve ser liberada em uma chamada para [xlFree](xlfree.md) depois que ele não é mais necessária, ou definindo **xlbitXLFree** se retorná-lo para o Excel.</span><span class="sxs-lookup"><span data-stu-id="d0484-120">Any memory pointed to in the result will have been allocated by Excel and should be freed in a call to [xlFree](xlfree.md) once it is no longer needed, or by setting **xlbitXLFree** if returning it to Excel.</span></span> 
  
 <span data-ttu-id="d0484-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="d0484-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="d0484-122">O número de argumentos que serão passadas para a função.</span><span class="sxs-lookup"><span data-stu-id="d0484-122">The number of arguments that will be passed to the function.</span></span> <span data-ttu-id="d0484-123">Iniciando no Excel 2007, o limite é 255 argumentos.</span><span class="sxs-lookup"><span data-stu-id="d0484-123">Starting in Excel 2007, the limit is 255 arguments.</span></span> <span data-ttu-id="d0484-124">Nas versões anteriores, o limite é 30.</span><span class="sxs-lookup"><span data-stu-id="d0484-124">In earlier versions, the limit is 30.</span></span>
  
 <span data-ttu-id="d0484-125">_Argumento1,..._</span><span class="sxs-lookup"><span data-stu-id="d0484-125">_argument1, ..._</span></span>
  
<span data-ttu-id="d0484-126">Os argumentos opcionais para a função.</span><span class="sxs-lookup"><span data-stu-id="d0484-126">The optional arguments to the function.</span></span> <span data-ttu-id="d0484-127">Todos os argumentos devem ser ponteiros para s **XLOPER**no caso do **Excel**ou **XLOPER12**s no caso de **Excel12f**.</span><span class="sxs-lookup"><span data-stu-id="d0484-127">All arguments must be pointers to **XLOPER**s in the case of **Excel**, or **XLOPER12**s in the case of **Excel12f**.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="d0484-128">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d0484-128">Return value</span></span>

<span data-ttu-id="d0484-129">Ambas as funções retornam o mesmo erro e códigos de sucesso como **Excel4**, **Excel4v**, **Excel12**e **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="d0484-129">Both functions return the same error and success codes as **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**.</span></span> <span data-ttu-id="d0484-130">Consulte [Excel4/Excel12](excel4-excel12.md) para obter uma descrição completa desses códigos.</span><span class="sxs-lookup"><span data-stu-id="d0484-130">See [Excel4/Excel12](excel4-excel12.md) for a full description of these codes.</span></span> <span data-ttu-id="d0484-131">Além disso, essas funções de Framework retornam **xlretFailed** sem chamar a API C se um ponteiro NULL a um parâmetro é detectado.</span><span class="sxs-lookup"><span data-stu-id="d0484-131">In addition, these Framework functions return **xlretFailed** without calling the C API if a NULL pointer to a parameter is detected.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d0484-132">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d0484-132">Example</span></span>

<span data-ttu-id="d0484-133">Este exemplo passa um argumento inválido para a função de **Excel12f** , que envia uma mensagem ao depurador.</span><span class="sxs-lookup"><span data-stu-id="d0484-133">This example passes a bad argument to the **Excel12f** function, which sends a message to the debugger.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="d0484-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0484-134">See also</span></span>



[<span data-ttu-id="d0484-135">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="d0484-135">Excel4/Excel12</span></span>](excel4-excel12.md)


[<span data-ttu-id="d0484-136">Funções na biblioteca de estrutura</span><span class="sxs-lookup"><span data-stu-id="d0484-136">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

