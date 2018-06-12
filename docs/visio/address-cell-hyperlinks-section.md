---
title: Célula Address (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
localization_priority: Normal
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: Especifica uma URL, um nome de arquivo ou um caminho UNC para o qual ir.
ms.openlocfilehash: 840ce0c4ce73da378f80e5d8a185073ac3915daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771272"
---
# <a name="address-cell-hyperlinks-section"></a><span data-ttu-id="1b214-103">Célula Address (Seção Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="1b214-103">Address Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="1b214-104">Especifica uma URL, um nome de arquivo ou um caminho UNC para o qual ir.</span><span class="sxs-lookup"><span data-stu-id="1b214-104">Specifies a URL address, file name, or UNC path to which to jump.</span></span>
  
<span data-ttu-id="1b214-105">Você pode especificar o endereço como um caminho relativo com base no caminho de base definido para o documento na caixa de **base do hiperlink** na guia **Resumo** da caixa de diálogo **Propriedades** (clique na guia **arquivo** , clique em **Info*** * propriedades * * e clique em **Propriedades avançadas**).</span><span class="sxs-lookup"><span data-stu-id="1b214-105">You can specify Address as a relative path based on the base path defined for the document in the **Hyperlink base** box on the **Summary** tab of the **Properties** dialog box (click the **File** tab, click **Info**, click ** Properties **, and then click **Advanced Properties**).</span></span> <span data-ttu-id="1b214-106">Se o documento não tiver nenhum caminho de base, o aplicativo navegará com base no caminho do documento.</span><span class="sxs-lookup"><span data-stu-id="1b214-106">If the document has no base path, the application navigates based on the document path.</span></span> <span data-ttu-id="1b214-107">Se o documento não tiver sido salvo, o hiperlink é indefinido.</span><span class="sxs-lookup"><span data-stu-id="1b214-107">If the document has not been saved, the hyperlink is undefined.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1b214-108">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="1b214-108">Remarks</span></span>

<span data-ttu-id="1b214-109">Você também pode definir o valor da célula Address na caixa de diálogo **hiperlinks** (clique em **hiperlink** na guia **Inserir** ).</span><span class="sxs-lookup"><span data-stu-id="1b214-109">You can also set the value of the Address cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="1b214-110">Para obter uma referência à célula Address pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="1b214-110">To get a reference to the Address cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b214-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="1b214-111">Cell name:</span></span>  <br/> |<span data-ttu-id="1b214-112">Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="1b214-112">Hyperlink.</span></span> <span data-ttu-id="1b214-113">*nome* . Endereços onde Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="1b214-113">*name*  .Address           where Hyperlink.</span></span> <span data-ttu-id="1b214-114">*nome* é o nome da linha do hiperlink</span><span class="sxs-lookup"><span data-stu-id="1b214-114">*name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="1b214-115">Para fazer referência à célula Address pelo nome, a partir de outra fórmula ou de um programa, usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="1b214-115">To get a reference to the Address cell by name from another formula, or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1b214-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="1b214-116">Section index:</span></span>  <br/> |<span data-ttu-id="1b214-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="1b214-117">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="1b214-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="1b214-118">Row index:</span></span>  <br/> |<span data-ttu-id="1b214-119">**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1b214-119">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1b214-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="1b214-120">Cell index:</span></span>  <br/> |<span data-ttu-id="1b214-121">**visHLinkAddress**</span><span class="sxs-lookup"><span data-stu-id="1b214-121">**visHLinkAddress**</span></span> <br/> |
   

