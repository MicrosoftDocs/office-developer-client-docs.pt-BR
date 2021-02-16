---
title: Função HYPERLINK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251441
localization_priority: Normal
ms.assetid: 943636a6-e135-a626-7924-11e238156548
description: Navega até o endereço especificado, que pode ser um arquivo, UNC ou caminho da URL.
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329943"
---
# <a name="hyperlink-function"></a><span data-ttu-id="eeea1-103">Função HYPERLINK</span><span class="sxs-lookup"><span data-stu-id="eeea1-103">HYPERLINK Function</span></span>

<span data-ttu-id="eeea1-104">Navega até o endereço especificado, que pode ser um arquivo, UNC ou caminho da URL.</span><span class="sxs-lookup"><span data-stu-id="eeea1-104">Navigates to the specified address, which can be a file, UNC, or URL path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="eeea1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eeea1-105">Syntax</span></span>

<span data-ttu-id="eeea1-106">HYPERLINK(" \*\* *endereço* \*\* "[," \*\* *subddress* \*\* "," \*\* *extrainfo* \*\* ", \*\* *window* \*\*," \*\* *frame* \*\* "])</span><span class="sxs-lookup"><span data-stu-id="eeea1-106">HYPERLINK(" \*\* *address* \*\* "[," \*\* *subaddress* \*\* "," \*\* *extrainfo* \*\* ", \*\* *window* \*\*," \*\* *frame* \*\* "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="eeea1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eeea1-107">Parameters</span></span>

|<span data-ttu-id="eeea1-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="eeea1-108">**Name**</span></span>|<span data-ttu-id="eeea1-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="eeea1-109">**Required/Optional**</span></span>|<span data-ttu-id="eeea1-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="eeea1-110">**Data Type**</span></span>|<span data-ttu-id="eeea1-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="eeea1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="eeea1-112">_address_</span><span class="sxs-lookup"><span data-stu-id="eeea1-112">_address_</span></span> <br/> |<span data-ttu-id="eeea1-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="eeea1-113">Required</span></span>  <br/> |<span data-ttu-id="eeea1-114">**String**</span><span class="sxs-lookup"><span data-stu-id="eeea1-114">**String**</span></span> <br/> |<span data-ttu-id="eeea1-115">Um caminho completo ou relativo.</span><span class="sxs-lookup"><span data-stu-id="eeea1-115">A full path or a relative path.</span></span>  <br/> |
| <span data-ttu-id="eeea1-116">_subaddress_</span><span class="sxs-lookup"><span data-stu-id="eeea1-116">_subaddress_</span></span> <br/> |<span data-ttu-id="eeea1-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="eeea1-117">Optional</span></span>  <br/> |<span data-ttu-id="eeea1-118">**String**</span><span class="sxs-lookup"><span data-stu-id="eeea1-118">**String**</span></span> <br/> |<span data-ttu-id="eeea1-119">Especifica uma localização no address ao qual se vincular.</span><span class="sxs-lookup"><span data-stu-id="eeea1-119">Specifies a location within address to link to.</span></span> <span data-ttu-id="eeea1-120">Por exemplo, se o address for um arquivo do Microsoft Visio, o subaddress poderá ser um nome de página; se for um arquivo do Microsoft Excel, o subaddress poderá ser uma planilha ou um intervalo na planilha; se for uma URL de uma página HTML, o subaddress poderá ser uma âncora.</span><span class="sxs-lookup"><span data-stu-id="eeea1-120">For example, if address is a Microsoft Visio file, subaddress can be a page name; if a Microsoft Excel file, subaddress can be a worksheet or range within a worksheet; if a URL for an HTML page, subaddress can be an anchor.</span></span>  <br/> |
| <span data-ttu-id="eeea1-121">_extrainfo_</span><span class="sxs-lookup"><span data-stu-id="eeea1-121">_extrainfo_</span></span> <br/> |<span data-ttu-id="eeea1-122">Opcional</span><span class="sxs-lookup"><span data-stu-id="eeea1-122">Optional</span></span>  <br/> |<span data-ttu-id="eeea1-123">**String**</span><span class="sxs-lookup"><span data-stu-id="eeea1-123">**String**</span></span> <br/> |<span data-ttu-id="eeea1-124">Passa as informações utilizadas para resolver o URL, como as coordenadas de um mapa de imagens.</span><span class="sxs-lookup"><span data-stu-id="eeea1-124">Passes information used in resolving the URL, such as the coordinates of an image map.</span></span>  <br/> |
| <span data-ttu-id="eeea1-125">_janela_</span><span class="sxs-lookup"><span data-stu-id="eeea1-125">_window_</span></span> <br/> |<span data-ttu-id="eeea1-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="eeea1-126">Optional</span></span>  <br/> |<span data-ttu-id="eeea1-127">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="eeea1-127">**Boolean**</span></span> <br/> |<span data-ttu-id="eeea1-128">Especifica se o hiperlink será aberto em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="eeea1-128">Specifies whether the hyperlink is opened in a new window.</span></span> <span data-ttu-id="eeea1-129">O valor padrão é FALSO.</span><span class="sxs-lookup"><span data-stu-id="eeea1-129">The default value is FALSE.</span></span>  <br/> |
| <span data-ttu-id="eeea1-130">_frame_</span><span class="sxs-lookup"><span data-stu-id="eeea1-130">_frame_</span></span> <br/> |<span data-ttu-id="eeea1-131">Opcional</span><span class="sxs-lookup"><span data-stu-id="eeea1-131">Optional</span></span>  <br/> |<span data-ttu-id="eeea1-132">**String**</span><span class="sxs-lookup"><span data-stu-id="eeea1-132">**String**</span></span> <br/> | <span data-ttu-id="eeea1-p103">Especifica o nome de uma moldura para servir de destino quando o Visio for aberto como um documento ativo em um navegador ActiveX, como o Microsoft Internet Explorer 3.0 ou superior. O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="eeea1-p103">Specifies the name of a frame to target when Visio is open as an Active document in an ActiveX browser, such as Microsoft Internet Explorer 3.0 or later. The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eeea1-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="eeea1-135">Remarks</span></span>

<span data-ttu-id="eeea1-p104">Se o documento não tiver caminho de base, o Visio navegará de acordo com o caminho do documento. Se o documento não tiver sido salvo, o hiperlink não será definido.</span><span class="sxs-lookup"><span data-stu-id="eeea1-p104">If the document has no base path, Visio navigates according to the document path. If the document has not been saved, the hyperlink is undefined.</span></span> 
  
<span data-ttu-id="eeea1-138">Caminhos relativos têm como base o campo **Base do Hiperlink** especificado na caixa de diálogo **Propriedades do Visio**.</span><span class="sxs-lookup"><span data-stu-id="eeea1-138">Relative paths are based on the **Hyperlink base** field specified in the **Visio Properties** dialog box.</span></span> 
  
<span data-ttu-id="eeea1-139">Utilize a função GOTOPAGE para navegar em páginas de um documento.</span><span class="sxs-lookup"><span data-stu-id="eeea1-139">You can use the GOTOPAGE function to navigate to pages of a document.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="eeea1-140">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eeea1-140">Example 1</span></span>

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a><span data-ttu-id="eeea1-141">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="eeea1-141">Example 2</span></span>

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a><span data-ttu-id="eeea1-142">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="eeea1-142">Example 3</span></span>

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a><span data-ttu-id="eeea1-143">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="eeea1-143">Example 4</span></span>

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

