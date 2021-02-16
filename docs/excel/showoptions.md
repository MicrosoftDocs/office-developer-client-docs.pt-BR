---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5b58b71dc4f2441448eb3e0dac2c3c5763675927
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407694"
---
# <a name="showoptions"></a><span data-ttu-id="aea9a-103">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="aea9a-103">ShowOptions</span></span>

<span data-ttu-id="aea9a-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="aea9a-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="aea9a-105">Mostra uma caixa de diálogo modal para coletar informações do usuário.</span><span class="sxs-lookup"><span data-stu-id="aea9a-105">Shows a modal dialog box to collect information from the user.</span></span> <span data-ttu-id="aea9a-106">Esse ponto de entrada é chamado  quando um  usuário clica no botão Opções ao lado da caixa  de tipo cluster para o conector de cluster selecionado na caixa de diálogo Opções do **Excel** (na categoria Avançado na seção **Fórmulas).**</span><span class="sxs-lookup"><span data-stu-id="aea9a-106">This entry point is called when a user clicks the **Options** button next to the **Cluster type** box for the selected cluster connector in the **Excel Options** dialog box (in the **Advanced** category under the **Formulas** section).</span></span> <span data-ttu-id="aea9a-107">Os conectores de cluster são responsáveis por implementar sua própria interface de diálogo de opções e por armazenar os dados relacionados no Registro ou em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="aea9a-107">Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere.</span></span> <span data-ttu-id="aea9a-108">As opções são internas ao conector do cluster.</span><span class="sxs-lookup"><span data-stu-id="aea9a-108">The options are internal to the cluster connector.</span></span> <span data-ttu-id="aea9a-109">O Excel não está ciente deles.</span><span class="sxs-lookup"><span data-stu-id="aea9a-109">Excel is not aware of them.</span></span> 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a><span data-ttu-id="aea9a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aea9a-110">Parameters</span></span>

<span data-ttu-id="aea9a-111">_hWndParent_</span><span class="sxs-lookup"><span data-stu-id="aea9a-111">_hWndParent_</span></span>
  
> <span data-ttu-id="aea9a-112">Um alça para a janela do Excel.</span><span class="sxs-lookup"><span data-stu-id="aea9a-112">A handle to the Excel window.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aea9a-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="aea9a-113">Return value</span></span>

<span data-ttu-id="aea9a-114">**xlHpcRetSuccess** se a caixa de diálogo foi mostrada; **xlHpcRetCallFailed** se não foi mostrado.</span><span class="sxs-lookup"><span data-stu-id="aea9a-114">**xlHpcRetSuccess** if the dialog box was shown; **xlHpcRetCallFailed** if it was not shown.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="aea9a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="aea9a-115">Remarks</span></span>

<span data-ttu-id="aea9a-116">Os conectores de cluster podem usar essa caixa de diálogo para obter informações, como qual servidor de cluster usar, do usuário.</span><span class="sxs-lookup"><span data-stu-id="aea9a-116">Cluster connectors can use this dialog box to get information, such as what cluster server to use, from the user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aea9a-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="aea9a-117">See also</span></span>

- [<span data-ttu-id="aea9a-118">Funções de conector de cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="aea9a-118">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

