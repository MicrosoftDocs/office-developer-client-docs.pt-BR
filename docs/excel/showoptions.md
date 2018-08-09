---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: dbf6f0f50e9f7fa988e83f3b58012e9deac13eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765437"
---
# <a name="showoptions"></a><span data-ttu-id="c0969-103">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="c0969-103">ShowOptions</span></span>

<span data-ttu-id="c0969-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c0969-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c0969-105">Mostra a caixa de diálogo modal para coletar informações do usuário.</span><span class="sxs-lookup"><span data-stu-id="c0969-105">Shows a modal dialog box to collect information from the user.</span></span> <span data-ttu-id="c0969-106">Esse ponto de entrada é chamado quando um usuário clica no botão de **Opções** ao lado da caixa **tipo de Cluster** para o conector de cluster selecionado na caixa de diálogo **Opções do Excel** (na categoria **Avançado** sob a seção de **fórmulas** ).</span><span class="sxs-lookup"><span data-stu-id="c0969-106">This entry point is called when a user clicks the **Options** button next to the **Cluster type** box for the selected cluster connector in the **Excel Options** dialog box (in the **Advanced** category under the **Formulas** section).</span></span> <span data-ttu-id="c0969-107">Conectores de cluster são responsáveis para implementar sua própria interface de diálogo Opções e para armazenar os dados relacionados no registro ou em outro local.</span><span class="sxs-lookup"><span data-stu-id="c0969-107">Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere.</span></span> <span data-ttu-id="c0969-108">As opções são internas para o conector de cluster.</span><span class="sxs-lookup"><span data-stu-id="c0969-108">The options are internal to the cluster connector.</span></span> <span data-ttu-id="c0969-109">Excel não está ciente deles.</span><span class="sxs-lookup"><span data-stu-id="c0969-109">Excel is not aware of them.</span></span> 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a><span data-ttu-id="c0969-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0969-110">Parameters</span></span>

<span data-ttu-id="c0969-111">_hWndParent_</span><span class="sxs-lookup"><span data-stu-id="c0969-111">_hWndParent_</span></span>
  
> <span data-ttu-id="c0969-112">Um identificador para a janela do Excel.</span><span class="sxs-lookup"><span data-stu-id="c0969-112">A handle to the Excel window.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c0969-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c0969-113">Return value</span></span>

<span data-ttu-id="c0969-114">**xlHpcRetSuccess** se a caixa de diálogo foi mostrada; **xlHpcRetCallFailed** se ele não foi exibido.</span><span class="sxs-lookup"><span data-stu-id="c0969-114">**xlHpcRetSuccess** if the dialog box was shown; **xlHpcRetCallFailed** if it was not shown.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c0969-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0969-115">Remarks</span></span>

<span data-ttu-id="c0969-116">Conectores de cluster podem usar esta caixa de diálogo para obter mais informações, como o que o servidor do cluster use, do usuário.</span><span class="sxs-lookup"><span data-stu-id="c0969-116">Cluster connectors can use this dialog box to get information, such as what cluster server to use, from the user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0969-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0969-117">See also</span></span>

- [<span data-ttu-id="c0969-118">Funções de conector de cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="c0969-118">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

