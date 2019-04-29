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
ms.openlocfilehash: 0fbb89e18a2d7a849e2369c0d41aac4a647f067b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438033"
---
# <a name="address-cell-hyperlinks-section"></a><span data-ttu-id="77c83-103">Célula Address (Seção Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="77c83-103">Address Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="77c83-104">Especifica uma URL, um nome de arquivo ou um caminho UNC para o qual ir.</span><span class="sxs-lookup"><span data-stu-id="77c83-104">Specifies a URL address, file name, or UNC path to which to jump.</span></span>
  
<span data-ttu-id="77c83-105">Você pode especificar o endereço como um caminho relativo com base no caminho base definido para o documento na **caixa base do hiperlink** na guia **Resumo** da caixa de diálogo **Propriedades** (clique na guia **arquivo** , em **informações**, em \* \* Propriedades \* \* e, em seguida, clique em **Propriedades avançadas**.</span><span class="sxs-lookup"><span data-stu-id="77c83-105">You can specify Address as a relative path based on the base path defined for the document in the **Hyperlink base** box on the **Summary** tab of the **Properties** dialog box (click the **File** tab, click **Info**, click \*\* Properties \*\*, and then click **Advanced Properties**).</span></span> <span data-ttu-id="77c83-106">Se o documento não contiver um caminho de base, o aplicativo navegará com base no caminho do documento.</span><span class="sxs-lookup"><span data-stu-id="77c83-106">If the document has no base path, the application navigates based on the document path.</span></span> <span data-ttu-id="77c83-107">Se o documento não tiver sido salvo, o hiperlink não será definido.</span><span class="sxs-lookup"><span data-stu-id="77c83-107">If the document has not been saved, the hyperlink is undefined.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="77c83-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="77c83-108">Remarks</span></span>

<span data-ttu-id="77c83-109">Você pode também definir o valor da célula Address na caixa de diálogo **Hiperlinks** (clique em **Hiperlink** na guia **Inserir**).</span><span class="sxs-lookup"><span data-stu-id="77c83-109">You can also set the value of the Address cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="77c83-110">Para fazer referência à célula Address pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="77c83-110">To get a reference to the Address cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77c83-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="77c83-111">Cell name:</span></span>  <br/> |<span data-ttu-id="77c83-112">Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="77c83-112">Hyperlink.</span></span> <span data-ttu-id="77c83-113">*nome* . Endereço onde hiperlink.</span><span class="sxs-lookup"><span data-stu-id="77c83-113">*name*  .Address           where Hyperlink.</span></span> <span data-ttu-id="77c83-114">*Name* é o nome da linha de hiperlink</span><span class="sxs-lookup"><span data-stu-id="77c83-114">*name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="77c83-115">Para fazer referência à célula address pelo nome, a partir de outra fórmula ou programa, usando a propriedade Cells \*\*\*\* , utilize:</span><span class="sxs-lookup"><span data-stu-id="77c83-115">To get a reference to the Address cell by name from another formula, or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="77c83-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="77c83-116">Section index:</span></span>  <br/> |<span data-ttu-id="77c83-117">**visSectionHiperlink**</span><span class="sxs-lookup"><span data-stu-id="77c83-117">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="77c83-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="77c83-118">Row index:</span></span>  <br/> |<span data-ttu-id="77c83-119">**visRow1stHyperlink** +  *i*            em que  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="77c83-119">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="77c83-120">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="77c83-120">Cell index:</span></span>  <br/> |<span data-ttu-id="77c83-121">**visHLinkAddress**</span><span class="sxs-lookup"><span data-stu-id="77c83-121">**visHLinkAddress**</span></span> <br/> |
   

