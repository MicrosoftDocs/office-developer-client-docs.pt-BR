---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- função xlautoadd [excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ae0b4ae2d5f5fc58c3e18ffa9d79ec4128cb4639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765448"
---
# <a name="xlautoadd"></a><span data-ttu-id="29358-104">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="29358-104">xlAutoAdd</span></span>

 <span data-ttu-id="29358-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="29358-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="29358-106">Adicionado pelo Microsoft Excel sempre que o usuário ativa o XLL durante uma sessão do Excel usando o Gerenciador de suplemento.</span><span class="sxs-lookup"><span data-stu-id="29358-106">Added by Microsoft Excel whenever the user activates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="29358-107">Essa função não é chamada quando o Excel é iniciado e carrega um suplemento pré-instaladas.</span><span class="sxs-lookup"><span data-stu-id="29358-107">This function is not called when Excel starts up and loads a pre-installed add-in.</span></span>
  
<span data-ttu-id="29358-108">Esta função pode ser usada para exibir uma caixa de diálogo personalizada que informa ao usuário que o suplemento tiver sido ativado, ou para ler ou gravar no registro ou verificar as informações de licenciamento, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="29358-108">This function can be used to display a custom dialog box that tells the user that the add-in has been activated, or to read from or write to the registry, or check licensing information, for example.</span></span>
  
<span data-ttu-id="29358-109">Excel não exige um XLL implementar e exportar essa função.</span><span class="sxs-lookup"><span data-stu-id="29358-109">Excel does not require an XLL to implement and export this function.</span></span>
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a><span data-ttu-id="29358-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29358-110">Parameters</span></span>

<span data-ttu-id="29358-111">Essa função não usa argumentos.</span><span class="sxs-lookup"><span data-stu-id="29358-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="29358-112">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="29358-112">Property value/Return value</span></span>

<span data-ttu-id="29358-113">A implementação dessa função deve retornar 1.</span><span class="sxs-lookup"><span data-stu-id="29358-113">Your implementation of this function should return 1.</span></span> <span data-ttu-id="29358-114">(**int**).</span><span class="sxs-lookup"><span data-stu-id="29358-114">(**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="29358-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="29358-115">Remarks</span></span>

<span data-ttu-id="29358-116">Use esta função se não houver nada que seu XLL precisa fazer quando ele é adicionado pelo gerente de suplemento.</span><span class="sxs-lookup"><span data-stu-id="29358-116">Use this function if there is anything your XLL needs to do when it is added by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="29358-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="29358-117">Example</span></span>

<span data-ttu-id="29358-118">Consulte `\SAMPLES\EXAMPLE\EXAMPLE.C` e `\SAMPLES\GENERIC\GENERIC.C` por exemplo implementações dessa função.</span><span class="sxs-lookup"><span data-stu-id="29358-118">See  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="29358-119">O código a seguir é de `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="29358-119">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
```cs
int WINAPI xlAutoAdd(void)
{
    XCHAR szBuf[255];
    wsprintfW((LPWSTR)szBuf, L"Thank you for adding Example.XLL\n"
            L"build date %hs, time %hs",__DATE__, __TIME__);
/* Display a dialog indicating that the XLL was successfully added */
    Excel12f(xlcAlert, 0, 2, TempStr12(szBuf), TempInt12(2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="29358-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="29358-120">See also</span></span>



[<span data-ttu-id="29358-121">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="29358-121">xlAutoRemove</span></span>](xlautoremove.md)


[<span data-ttu-id="29358-122">Gerenciador de Suplemento e Funções da Interface XLL</span><span class="sxs-lookup"><span data-stu-id="29358-122">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

