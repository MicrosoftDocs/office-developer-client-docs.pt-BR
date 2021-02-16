---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- Função xlgetinst [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e113ddbf55e2b4651d578549802c44e2c6413a18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428127"
---
# <a name="xlgetinst"></a><span data-ttu-id="e500b-104">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="e500b-104">xlGetInst</span></span>

 <span data-ttu-id="e500b-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e500b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e500b-106">Retorna o alça de instância da instância do Microsoft Excel que está chamando uma DLL no momento.</span><span class="sxs-lookup"><span data-stu-id="e500b-106">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="e500b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e500b-107">Parameters</span></span>

<span data-ttu-id="e500b-108">Esta função não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="e500b-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e500b-109">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e500b-109">Property value/Return value</span></span>

<span data-ttu-id="e500b-110">O alça de instância (**xltypeInt**) estará no **campo val.w.**</span><span class="sxs-lookup"><span data-stu-id="e500b-110">The instance handle (**xltypeInt**) will be in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e500b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e500b-111">Remarks</span></span>

<span data-ttu-id="e500b-112">Essa função pode ser usada para distinguir entre várias instâncias em execução do Excel que estão chamando a DLL.</span><span class="sxs-lookup"><span data-stu-id="e500b-112">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="e500b-113">Quando você está chamando essa função usando [Excel4](excel4-excel12.md) ou [Excel4v](excel4v-excel12v.md), a variável de inteiro XLOPER retornada é um int de 16 bits curto assinado. Isso só é capaz de conter os 16 bits baixos do alça do Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e500b-113">When you are calling this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="e500b-114">A partir do Excel 2007, a variável inteira do **XLOPER12** é um int de 32 bits assinado e, portanto, contém o alça inteira, removendo a necessidade de iterar todas as janelas abertas.</span><span class="sxs-lookup"><span data-stu-id="e500b-114">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e500b-115">Se a **função xlGetInst** for usada com a versão de 64 bits do Microsoft Excel, a função falhará.</span><span class="sxs-lookup"><span data-stu-id="e500b-115">If the **xlGetInst** function is used with the 64-bit version of Microsoft Excel, then the function will fail.</span></span> <span data-ttu-id="e500b-116">Isso ocorre porque o tipo **de valor xltypeInt** não é largo o suficiente para manter a alça longa de 64 bits retornada pelo Excel nesse caso.</span><span class="sxs-lookup"><span data-stu-id="e500b-116">This is because the **xltypeInt** value type is not wide enough to hold the 64-bit long handle returned by Excel in this case.</span></span> <span data-ttu-id="e500b-117">Para essa finalidade, o Excel 2010 introduziu uma nova função chamada [xlGetInstPtr](xlgetinstptr.md), que é executado corretamente com as versões de 32 bits e 64 bits do Excel.</span><span class="sxs-lookup"><span data-stu-id="e500b-117">For this purpose, Excel 2010 introduced a new function named [xlGetInstPtr](xlgetinstptr.md), which runs correctly with both the 32-bit and 64-bit versions of Excel.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e500b-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e500b-118">Example</span></span>

<span data-ttu-id="e500b-119">O exemplo a seguir compara a instância da última cópia do Excel que a chamou à cópia atual do Excel que a chamou.</span><span class="sxs-lookup"><span data-stu-id="e500b-119">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="e500b-120">Se eles são iguais, retornará 1; caso não seja, retornará 0; se a função falhar, retornará -1.</span><span class="sxs-lookup"><span data-stu-id="e500b-120">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInst, &xRes, 0) != xlretSuccess)
        iRet = -1;
    else
    {
    HANDLE hNew;
    hNew = (HANDLE)xRes.val.w;
    if (hNew != hOld)
            iRet = 0;
    else
            iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a><span data-ttu-id="e500b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e500b-121">See also</span></span>



[<span data-ttu-id="e500b-122">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="e500b-122">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="e500b-123">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="e500b-123">xlGetInstPtr</span></span>](xlgetinstptr.md)


[<span data-ttu-id="e500b-124">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="e500b-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

