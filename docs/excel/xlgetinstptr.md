---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7cc07093e5db335d01fe85527746594d34d4d938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765486"
---
# <a name="xlgetinstptr"></a><span data-ttu-id="a6aff-103">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="a6aff-103">xlGetInstPtr</span></span>

<span data-ttu-id="a6aff-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a6aff-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a6aff-105">Retorna o identificador de instância da instância do Microsoft Excel que atualmente está chamando uma DLL.</span><span class="sxs-lookup"><span data-stu-id="a6aff-105">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="a6aff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6aff-106">Parameters</span></span>

<span data-ttu-id="a6aff-107">Essa função não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="a6aff-107">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a6aff-108">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a6aff-108">Property value/Return value</span></span>

<span data-ttu-id="a6aff-109">O identificador de instância (**xltypeBigData**) será no campo **val.bigdata.h.hdata** .</span><span class="sxs-lookup"><span data-stu-id="a6aff-109">The instance handle (**xltypeBigData**) will be in the **val.bigdata.h.hdata** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a6aff-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6aff-110">Remarks</span></span>

<span data-ttu-id="a6aff-111">Esta função pode ser usada para distinguir entre várias instâncias em execução do Excel que estão chamando a DLL.</span><span class="sxs-lookup"><span data-stu-id="a6aff-111">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="a6aff-112">Essa função retornará um valor correto com versões de 32 bits e 64 bits do Excel.</span><span class="sxs-lookup"><span data-stu-id="a6aff-112">This function returns a correct value with both 32-bit and 64-bit versions of Excel.</span></span> <span data-ttu-id="a6aff-113">Ele foi introduzido no Excel 2010 como uma extensão para a função de [xlGetInst](xlgetinst.md) , que funciona corretamente apenas com as versões de 32 bits do Excel.</span><span class="sxs-lookup"><span data-stu-id="a6aff-113">It was introduced in Excel 2010 as an extension to the [xlGetInst](xlgetinst.md) function, which works correctly only with 32-bit versions of Excel.</span></span> 
  
<span data-ttu-id="a6aff-114">Essa função funciona corretamente quando ele é chamado usando as variedades [Excel4 e Excel12](excel4-excel12.md) das funções de retorno de chamada de API, porque **XLOPER** e **XLOPER12** tem a mesma estrutura que suporta o valor de **xltypeBigData** Digite.</span><span class="sxs-lookup"><span data-stu-id="a6aff-114">This function works correctly when it is called by using both the [Excel4 and Excel12](excel4-excel12.md) varieties of the API callback functions, because both **XLOPER** and **XLOPER12** have the same structure that supports the **xltypeBigData** value type.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a6aff-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a6aff-115">Example</span></span>

<span data-ttu-id="a6aff-116">O exemplo a seguir compara a instância da última cópia do Excel que a chamou com a cópia atual do Excel que a chamou.</span><span class="sxs-lookup"><span data-stu-id="a6aff-116">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="a6aff-117">Se eles forem iguais, ele retornará 1; Caso contrário, retornará 0; Se a função falhar, ele retornará -1.</span><span class="sxs-lookup"><span data-stu-id="a6aff-117">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span> <span data-ttu-id="a6aff-118">Este exemplo funciona com versões de 32 bits e 64 bits do Excel.</span><span class="sxs-lookup"><span data-stu-id="a6aff-118">This sample works with both 32-bit and 64-bit versions of Excel.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="a6aff-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6aff-119">See also</span></span>

- [<span data-ttu-id="a6aff-120">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="a6aff-120">xlGetHwnd</span></span>](xlgethwnd.md)
- [<span data-ttu-id="a6aff-121">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="a6aff-121">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="a6aff-122">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="a6aff-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

