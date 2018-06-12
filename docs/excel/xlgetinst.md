---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- função xlgetinst [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9484f7bbc1f5e0fc5b0def17f2ce79ef226dcd17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765474"
---
# <a name="xlgetinst"></a><span data-ttu-id="55720-104">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="55720-104">xlGetInst</span></span>

 <span data-ttu-id="55720-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="55720-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="55720-106">Retorna o identificador de instância da instância do Microsoft Excel que atualmente está chamando uma DLL.</span><span class="sxs-lookup"><span data-stu-id="55720-106">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="55720-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="55720-107">Parameters</span></span>

<span data-ttu-id="55720-108">Essa função não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="55720-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="55720-109">Propriedade valor/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="55720-109">Property value/Return value</span></span>

<span data-ttu-id="55720-110">O identificador de instância (**xltypeInt**) será no campo **val.w** .</span><span class="sxs-lookup"><span data-stu-id="55720-110">The instance handle (**xltypeInt**) will be in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="55720-111">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="55720-111">Remarks</span></span>

<span data-ttu-id="55720-112">Esta função pode ser usada para distinguir entre várias instâncias em execução do Excel que estão chamando a DLL.</span><span class="sxs-lookup"><span data-stu-id="55720-112">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="55720-113">Quando você chama essa função usando [Excel4](excel4-excel12.md) ou [Excel4v](excel4v-excel12v.md), a variável de inteiro XLOPER retornada é um curto int 16 bits assinado, a. Isso só é capaz de conter os 16 bits baixos da alça de Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="55720-113">When you are calling this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="55720-114">Iniciando no Excel 2007, a variável de inteiro de **XLOPER12** é um int assinado de 32 bits e, portanto, contém um manipulador de inteiro, removendo a necessidade de iterar todas as janelas abertas.</span><span class="sxs-lookup"><span data-stu-id="55720-114">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="55720-115">Se a função **xlGetInst** é usada com a versão de 64 bits do Microsoft Excel, a função falhará.</span><span class="sxs-lookup"><span data-stu-id="55720-115">If the **xlGetInst** function is used with the 64-bit version of Microsoft Excel, then the function will fail.</span></span> <span data-ttu-id="55720-116">Isso ocorre porque o tipo de valor **xltypeInt** não é ampla o suficiente para armazenar a alça de 64 bits longa retornada pelo Excel neste caso.</span><span class="sxs-lookup"><span data-stu-id="55720-116">This is because the **xltypeInt** value type is not wide enough to hold the 64-bit long handle returned by Excel in this case.</span></span> <span data-ttu-id="55720-117">Para esse fim, o Excel 2010 introduziu uma nova função chamada [xlGetInstPtr](xlgetinstptr.md), que é executado corretamente com as versões 32 bits e 64 bits do Excel.</span><span class="sxs-lookup"><span data-stu-id="55720-117">For this purpose, Excel 2010 introduced a new function named [xlGetInstPtr](xlgetinstptr.md), which runs correctly with both the 32-bit and 64-bit versions of Excel.</span></span> 
  
## <a name="example"></a><span data-ttu-id="55720-118">Example</span><span class="sxs-lookup"><span data-stu-id="55720-118">Example</span></span>

<span data-ttu-id="55720-119">O exemplo a seguir compara a instância da última cópia do Excel que a chamou com a cópia atual do Excel que a chamou.</span><span class="sxs-lookup"><span data-stu-id="55720-119">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="55720-120">Se eles forem iguais, ele retornará 1; Caso contrário, retornará 0; Se a função falhar, ele retornará -1.</span><span class="sxs-lookup"><span data-stu-id="55720-120">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="55720-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="55720-121">See also</span></span>



[<span data-ttu-id="55720-122">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="55720-122">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="55720-123">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="55720-123">xlGetInstPtr</span></span>](xlgetinstptr.md)


[<span data-ttu-id="55720-124">Funções da API C que podem ser chamadas apenas por um DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="55720-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

