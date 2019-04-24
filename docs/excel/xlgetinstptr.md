---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fd4b4ad5bf52f29384ef7e0ba738c350189f471e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310049"
---
# <a name="xlgetinstptr"></a><span data-ttu-id="4f2fa-103">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="4f2fa-103">xlGetInstPtr</span></span>

<span data-ttu-id="4f2fa-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4f2fa-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4f2fa-105">Retorna o identificador de instância da instância do Microsoft Excel que está atualmente chamando uma DLL.</span><span class="sxs-lookup"><span data-stu-id="4f2fa-105">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="4f2fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f2fa-106">Parameters</span></span>

<span data-ttu-id="4f2fa-107">Esta função não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="4f2fa-107">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="4f2fa-108">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4f2fa-108">Property value/Return value</span></span>

<span data-ttu-id="4f2fa-109">O identificador de instância (**xltypeBigData**) será no campo **Val. bigdata. h. hData** .</span><span class="sxs-lookup"><span data-stu-id="4f2fa-109">The instance handle (**xltypeBigData**) will be in the **val.bigdata.h.hdata** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4f2fa-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f2fa-110">Remarks</span></span>

<span data-ttu-id="4f2fa-111">Essa função pode ser usada para distinguir entre várias instâncias em execução do Excel que estão chamando a DLL.</span><span class="sxs-lookup"><span data-stu-id="4f2fa-111">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="4f2fa-112">Essa função retorna um valor correto com as versões de 32 bits e 64 bits do Excel.</span><span class="sxs-lookup"><span data-stu-id="4f2fa-112">This function returns a correct value with both 32-bit and 64-bit versions of Excel.</span></span> <span data-ttu-id="4f2fa-113">Ele foi introduzido no Excel 2010 como uma extensão para a função [xlGetInst](xlgetinst.md) , que funciona corretamente apenas com as versões de 32 bits do Excel.</span><span class="sxs-lookup"><span data-stu-id="4f2fa-113">It was introduced in Excel 2010 as an extension to the [xlGetInst](xlgetinst.md) function, which works correctly only with 32-bit versions of Excel.</span></span> 
  
<span data-ttu-id="4f2fa-114">Essa função funciona corretamente quando é chamada usando o [Excel4 e o Excel12](excel4-excel12.md) variedades das funções de retorno de chamada da API, porque **XLOPER** e **XLOPER12** têm a mesma estrutura que dá suporte ao valor **xltypeBigData** Escreva.</span><span class="sxs-lookup"><span data-stu-id="4f2fa-114">This function works correctly when it is called by using both the [Excel4 and Excel12](excel4-excel12.md) varieties of the API callback functions, because both **XLOPER** and **XLOPER12** have the same structure that supports the **xltypeBigData** value type.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4f2fa-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4f2fa-115">Example</span></span>

<span data-ttu-id="4f2fa-116">O exemplo a seguir compara a instância da última cópia do Excel que a chamou para a cópia atual do Excel que a chamou.</span><span class="sxs-lookup"><span data-stu-id="4f2fa-116">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="4f2fa-117">Se forem iguais, retornará 1; caso contrário, retornará 0; se a função falhar, ela retornará-1.</span><span class="sxs-lookup"><span data-stu-id="4f2fa-117">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span> <span data-ttu-id="4f2fa-118">Este exemplo funciona com as versões de 32 bits e 64 bits do Excel.</span><span class="sxs-lookup"><span data-stu-id="4f2fa-118">This sample works with both 32-bit and 64-bit versions of Excel.</span></span>
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstPtrExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInstPtr, &xRes, 0) != xlretSuccess)
    iRet = -1;
    else
    {
    HANDLE hNew;
    hNew =  xRes.val.bigdata.h.hdata;
    if (hNew != hOld)
    iRet = 0;
    else
    iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a><span data-ttu-id="4f2fa-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f2fa-119">See also</span></span>

- [<span data-ttu-id="4f2fa-120">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="4f2fa-120">xlGetHwnd</span></span>](xlgethwnd.md)
- [<span data-ttu-id="4f2fa-121">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="4f2fa-121">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="4f2fa-122">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="4f2fa-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

