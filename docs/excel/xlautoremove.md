---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- Função xlautoremove [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8bd2d44883b1820be42b82d4fe4794fa29caab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425474"
---
# <a name="xlautoremove"></a><span data-ttu-id="94a8e-104">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="94a8e-104">xlAutoRemove</span></span>

 <span data-ttu-id="94a8e-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="94a8e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="94a8e-106">Chamado pelo Microsoft Excel sempre que o usuário desativa o XLL durante uma sessão do Excel usando o Add-In Manager.</span><span class="sxs-lookup"><span data-stu-id="94a8e-106">Called by Microsoft Excel whenever the user deactivates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="94a8e-107">Esta função não é chamada quando uma sessão do Excel é fechada, normalmente ou de forma anormal, com o suplemento instalado.</span><span class="sxs-lookup"><span data-stu-id="94a8e-107">This function is not called when an Excel session closes, normally or abnormally, with the add-in installed.</span></span>
  
<span data-ttu-id="94a8e-108">Essa função pode ser usada para exibir uma caixa de diálogo personalizada que diz ao usuário que o complemento foi desativado ou para ler ou gravar no Registro, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="94a8e-108">This function can be used to display a custom dialog box telling the user that the add-in has been deactivated, or to read from or write to the registry, for example.</span></span>
  
<span data-ttu-id="94a8e-109">O Excel não exige um XLL para implementar e exportar essa função.</span><span class="sxs-lookup"><span data-stu-id="94a8e-109">Excel does not require an XLL to implement and export this function.</span></span> 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a><span data-ttu-id="94a8e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94a8e-110">Parameters</span></span>

<span data-ttu-id="94a8e-111">Essa função não usa argumentos.</span><span class="sxs-lookup"><span data-stu-id="94a8e-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="94a8e-112">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="94a8e-112">Property value/Return value</span></span>

<span data-ttu-id="94a8e-113">A implementação dessa função deve retornar 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="94a8e-113">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94a8e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="94a8e-114">Remarks</span></span>

<span data-ttu-id="94a8e-115">Use essa função se o XLL precisar concluir qualquer tarefa quando ela for removida pelo Add-In Manager.</span><span class="sxs-lookup"><span data-stu-id="94a8e-115">Use this function if your XLL needs to complete any task when it is removed by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="94a8e-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="94a8e-116">Example</span></span>

<span data-ttu-id="94a8e-117">Veja os arquivos `\SAMPLES\EXAMPLE\EXAMPLE.C` e `\SAMPLES\GENERIC\GENERIC.C` como exemplos de implementações dessa função.</span><span class="sxs-lookup"><span data-stu-id="94a8e-117">See the files  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="94a8e-118">O código a seguir é de `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="94a8e-118">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
```cs
int WINAPI xlAutoRemove(void)
{
/* Display a dialog box indicating that the XLL was successfully removed */
   Excel12f(xlcAlert, 0, 2,
      TempStr12(L"Thank you for removing Example.XLL!"),
      TempInt12(2));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="94a8e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="94a8e-119">See also</span></span>



[<span data-ttu-id="94a8e-120">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="94a8e-120">xlAutoAdd</span></span>](xlautoadd.md)


[<span data-ttu-id="94a8e-121">Gerenciador de Suplemento e Funções da Interface XLL</span><span class="sxs-lookup"><span data-stu-id="94a8e-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

