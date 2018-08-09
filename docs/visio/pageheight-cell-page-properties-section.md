---
title: Célula PageHeight (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm760
localization_priority: Normal
ms.assetid: 0184814c-2d67-6ad4-e336-5694612e518d
description: Contém a altura da página impressa em unidades de desenho.
ms.openlocfilehash: e198e90e9c70aad1e41ee02d5dcefea68846486c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772447"
---
# <a name="pageheight-cell-page-properties-section"></a><span data-ttu-id="54d12-103">Célula PageHeight (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="54d12-103">PageHeight Cell (Page Properties Section)</span></span>

<span data-ttu-id="54d12-104">Contém a altura da página impressa em unidades de desenho.</span><span class="sxs-lookup"><span data-stu-id="54d12-104">Contains the height of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54d12-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="54d12-105">Remarks</span></span>

<span data-ttu-id="54d12-106">Também é possível definir a altura da página na guia **Tamanho da Página** da caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página**) ou redimensionar manualmente a página com o mouse.</span><span class="sxs-lookup"><span data-stu-id="54d12-106">You can also set the page height on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow), or by manually resizing the page with the mouse.</span></span> 
  
<span data-ttu-id="54d12-107">Para obter uma referência para a célula PageHeight pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="54d12-107">To get a reference to the PageHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54d12-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="54d12-108">Cell name:</span></span>  <br/> |<span data-ttu-id="54d12-109">PageHeight</span><span class="sxs-lookup"><span data-stu-id="54d12-109">PageHeight</span></span>  <br/> |
   
<span data-ttu-id="54d12-110">Para obter uma referência para a célula PageHeight pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="54d12-110">To get a reference to the PageHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54d12-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="54d12-111">Section index:</span></span>  <br/> |<span data-ttu-id="54d12-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="54d12-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="54d12-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="54d12-113">Row index:</span></span>  <br/> |<span data-ttu-id="54d12-114">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="54d12-114">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="54d12-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="54d12-115">Cell index:</span></span>  <br/> |<span data-ttu-id="54d12-116">**visPageHeight**</span><span class="sxs-lookup"><span data-stu-id="54d12-116">**visPageHeight**</span></span> <br/> |
   

