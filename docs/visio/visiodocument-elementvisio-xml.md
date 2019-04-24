---
title: Elemento VisioDocument (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: O elemento raiz de um documento do Microsoft Visio.
ms.openlocfilehash: 9829fa8960d78777e0fff4306b96978da90a647d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285310"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="6953a-103">Elemento VisioDocument (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="6953a-103">VisioDocument element ('Visio XML')</span></span>

<span data-ttu-id="6953a-104">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="6953a-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6953a-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="6953a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6953a-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6953a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6953a-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="6953a-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6953a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6953a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6953a-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6953a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6953a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6953a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6953a-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="6953a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6953a-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="6953a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6953a-113">Definição</span><span class="sxs-lookup"><span data-stu-id="6953a-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6953a-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6953a-114">Elements and attributes</span></span>

<span data-ttu-id="6953a-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6953a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6953a-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6953a-116">Parent elements</span></span>

<span data-ttu-id="6953a-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6953a-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6953a-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6953a-118">Child elements</span></span>

|<span data-ttu-id="6953a-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6953a-119">**Element**</span></span>|<span data-ttu-id="6953a-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6953a-120">**Type**</span></span>|<span data-ttu-id="6953a-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6953a-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6953a-122">Colors</span><span class="sxs-lookup"><span data-stu-id="6953a-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6953a-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="6953a-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6953a-124">Contém a tabela de cor do documento.</span><span class="sxs-lookup"><span data-stu-id="6953a-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="6953a-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="6953a-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6953a-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="6953a-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6953a-127">Contém elementos que especificam configurações de documentos.</span><span class="sxs-lookup"><span data-stu-id="6953a-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="6953a-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="6953a-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6953a-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="6953a-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6953a-130">Especifica a estrutura **ShapeSheet** de um documento.</span><span class="sxs-lookup"><span data-stu-id="6953a-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="6953a-131">EventList</span><span class="sxs-lookup"><span data-stu-id="6953a-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6953a-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="6953a-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6953a-133">Contém um elemento **EventItem** para cada evento ao qual um objeto deve responder.</span><span class="sxs-lookup"><span data-stu-id="6953a-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="6953a-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="6953a-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6953a-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="6953a-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6953a-136">Contém uma coleção de elementos **FaceName**.</span><span class="sxs-lookup"><span data-stu-id="6953a-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="6953a-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="6953a-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6953a-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="6953a-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6953a-139">Contém elementos do cabeçalho e rodapé de um documento.</span><span class="sxs-lookup"><span data-stu-id="6953a-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="6953a-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="6953a-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6953a-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="6953a-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6953a-142">Especifica o conjunto de páginas de desenho que são visíveis e os conjuntos de registros que são atualizáveis em um desenho.</span><span class="sxs-lookup"><span data-stu-id="6953a-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="6953a-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="6953a-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6953a-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="6953a-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6953a-145">Contém uma coleção de elementos StyleSheet para o documento.</span><span class="sxs-lookup"><span data-stu-id="6953a-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6953a-146">Atributos</span><span class="sxs-lookup"><span data-stu-id="6953a-146">Attributes</span></span>

<span data-ttu-id="6953a-147">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="6953a-147">None.</span></span>
  

