---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- função xlFree [excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2dd61ee5cd0e2e671cc47425689287b8a437732f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765476"
---
# <a name="xlfree"></a><span data-ttu-id="f651b-104">xlFree</span><span class="sxs-lookup"><span data-stu-id="f651b-104">xlFree</span></span>

 <span data-ttu-id="f651b-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f651b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f651b-106">Usado para liberar memória recursos alocados pelo Microsoft Excel ao criar o retorno do valor **XLOPER**/ **XLOPER12** em uma chamada para [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)ou [Excel12v](excel4v-excel12v.md).</span><span class="sxs-lookup"><span data-stu-id="f651b-106">Used to free memory resources allocated by Microsoft Excel when creating the return value **XLOPER**/ **XLOPER12** in a call to [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), or [Excel12v](excel4v-excel12v.md).</span></span> <span data-ttu-id="f651b-107">A função **xlFree** libera a memória auxiliar e redefine o ponteiro para **Nulo** , mas não destruir outras partes da **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="f651b-107">The **xlFree** function frees the auxiliary memory and resets the pointer to **NULL** but does not destroy other parts of the **XLOPER**/ **XLOPER12**.</span></span>
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a><span data-ttu-id="f651b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f651b-108">Parameters</span></span>

 <span data-ttu-id="f651b-109">_px_1,..., px_n_</span><span class="sxs-lookup"><span data-stu-id="f651b-109">_px_1, ..., px_n_</span></span>
  
<span data-ttu-id="f651b-110">Um ou mais **XLOPER**/ **XLOPER12**s serem liberados.</span><span class="sxs-lookup"><span data-stu-id="f651b-110">One or more **XLOPER**/ **XLOPER12**s to be freed.</span></span> <span data-ttu-id="f651b-111">Nas versões do Excel até 2003, o número máximo de ponteiros que podem ser passados é 30.</span><span class="sxs-lookup"><span data-stu-id="f651b-111">In Excel versions up to 2003, the maximum number of pointers that can be passed is 30.</span></span> <span data-ttu-id="f651b-112">Iniciando no Excel 2007, isso é aumentado para 255.</span><span class="sxs-lookup"><span data-stu-id="f651b-112">Starting in Excel 2007, this is increased to 255.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f651b-113">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f651b-113">Property value/Return value</span></span>

<span data-ttu-id="f651b-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f651b-114">This function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f651b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f651b-115">Remarks</span></span>

<span data-ttu-id="f651b-116">Você deve liberar cada **XLOPER** que você obtenha um valor de retorno do **Excel4** ou **Excel4v** e cada **XLOPER12** que você obteve como um valor de retorno de **Excel12** ou **Excel12v** se eles são um dos seguintes tipos: xltypeStr ** **, **xltypeMulti**ou **xltypeRef**.</span><span class="sxs-lookup"><span data-stu-id="f651b-116">You must free every **XLOPER** that you get as a return value from **Excel4** or **Excel4v** and every **XLOPER12** that you get as a return value from **Excel12** or **Excel12v** if they are one of the following types: **xltypeStr**, **xltypeMulti**, or **xltypeRef**.</span></span> <span data-ttu-id="f651b-117">É sempre seguro liberar outros tipos, mesmo se eles não usar memória auxiliar, desde que você obteve-los do **Excel4** ou **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="f651b-117">It is always safe to free other types even if they do not use auxiliary memory, as long as you got them from **Excel4** or **Excel12**.</span></span>
  
<span data-ttu-id="f651b-118">Onde você está retornando ao Excel um ponteiro para um **XLOPER**/ **XLOPER12** que ainda contém memória alocada para Excel serem liberados, você deve definir o **xlbitXLFree** para garantir a memória de versões do Excel.</span><span class="sxs-lookup"><span data-stu-id="f651b-118">Where you are returning to Excel a pointer to an **XLOPER**/ **XLOPER12** that still contains Excel-allocated memory to be freed, you must set the **xlbitXLFree** to ensure Excel releases the memory.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f651b-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f651b-119">Example</span></span>

<span data-ttu-id="f651b-120">Este exemplo chama **Obtenha. WORKSPACE(1)** para retornar a plataforma na qual Excel está sendo executado como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f651b-120">This example calls **GET.WORKSPACE(1)** to return the platform on which Excel is currently running as a string.</span></span> <span data-ttu-id="f651b-121">O código copia isso retornou a cadeia de caracteres em um buffer para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="f651b-121">The code copies this returned string into a buffer for later use.</span></span> <span data-ttu-id="f651b-122">O código coloca o buffer de volta à **XLOPER12** para uso posterior com a função do Excel.</span><span class="sxs-lookup"><span data-stu-id="f651b-122">The code places the buffer back into the **XLOPER12** for later use with the Excel function.</span></span> <span data-ttu-id="f651b-123">Finalmente, o código exibirá a cadeia de caracteres em uma caixa de alerta.</span><span class="sxs-lookup"><span data-stu-id="f651b-123">Finally, the code displays the string in an alert box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlFreeExample(void)
{
   XLOPER12 xRes, xInt;
   XCHAR buffer[cchMaxStz];
   int i,len;
   // Create an XLOPER12 for the argument to Getworkspace.
   xInt.xltype = xltypeInt;
   xInt.val.w = 1;
   // Call GetWorkspace.
   Excel12f(xlfGetWorkspace, &xRes, 1, (LPXLOPER12)&xInt);
   
   // Get the length of the returned string
   len = (int)xRes.val.str[0];
   //Take into account 1st char, which contains the length
   //and the null terminator. Truncate if necessary to fit
   //buffer.
   if (len > cchMaxStz - 2)
      len = cchMaxStz - 2;
   // Copy to buffer.
   for(i = 1; i <= len; i++)
      buffer[i] = xRes.val.str[i];
   // Null terminate, Not necessary but a good idea.
   buffer[len] = '\0';
   buffer[0] = len;
   // Free the string returned from Excel.
   Excel12f(xlFree, 0, 1, &xRes);
   // Create a new string XLOPER12 for the alert.
   xRes.xltype = xltypeStr;
   xRes.val.str = buffer;
   // Show the alert.
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="f651b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f651b-124">See also</span></span>

- [<span data-ttu-id="f651b-125">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="f651b-125">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

