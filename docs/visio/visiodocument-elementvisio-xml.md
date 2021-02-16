---
title: Elemento VisioDocument (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: O elemento raiz de um documento do Microsoft Visio.
ms.openlocfilehash: acb0a4e8ef1efb6d6d5872118241e36bb4e9630c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538484"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="93f5e-103">Elemento VisioDocument (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="93f5e-103">VisioDocument element (Visio XML)</span></span>

<span data-ttu-id="93f5e-104">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="93f5e-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="93f5e-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="93f5e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93f5e-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="93f5e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="93f5e-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="93f5e-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="93f5e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="93f5e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="93f5e-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="93f5e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="93f5e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="93f5e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="93f5e-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="93f5e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="93f5e-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="93f5e-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="93f5e-113">Definição</span><span class="sxs-lookup"><span data-stu-id="93f5e-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="93f5e-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="93f5e-114">Elements and attributes</span></span>

<span data-ttu-id="93f5e-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="93f5e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="93f5e-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="93f5e-116">Parent elements</span></span>

<span data-ttu-id="93f5e-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="93f5e-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="93f5e-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="93f5e-118">Child elements</span></span>

|<span data-ttu-id="93f5e-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="93f5e-119">**Element**</span></span>|<span data-ttu-id="93f5e-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="93f5e-120">**Type**</span></span>|<span data-ttu-id="93f5e-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="93f5e-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="93f5e-122">Colors</span><span class="sxs-lookup"><span data-stu-id="93f5e-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93f5e-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="93f5e-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93f5e-124">Contém a tabela de cor do documento.</span><span class="sxs-lookup"><span data-stu-id="93f5e-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="93f5e-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="93f5e-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93f5e-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="93f5e-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93f5e-127">Contém elementos que especificam configurações de documentos.</span><span class="sxs-lookup"><span data-stu-id="93f5e-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="93f5e-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="93f5e-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93f5e-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="93f5e-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93f5e-130">Especifica a estrutura **ShapeSheet de um** documento.</span><span class="sxs-lookup"><span data-stu-id="93f5e-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="93f5e-131">EventList</span><span class="sxs-lookup"><span data-stu-id="93f5e-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93f5e-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="93f5e-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93f5e-133">Contém um elemento **EventItem** para cada evento ao qual um objeto deve responder.</span><span class="sxs-lookup"><span data-stu-id="93f5e-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="93f5e-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="93f5e-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93f5e-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="93f5e-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93f5e-136">Contém uma coleção de elementos **FaceName**.</span><span class="sxs-lookup"><span data-stu-id="93f5e-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="93f5e-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="93f5e-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93f5e-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="93f5e-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93f5e-139">Contém elementos para o rodapé e o rodapé de um documento.</span><span class="sxs-lookup"><span data-stu-id="93f5e-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="93f5e-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="93f5e-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93f5e-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="93f5e-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93f5e-142">Especifica o conjunto de páginas de desenho que são exibiveis e um conjunto de recordsets que são atualizáveis em um desenho.</span><span class="sxs-lookup"><span data-stu-id="93f5e-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="93f5e-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="93f5e-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93f5e-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="93f5e-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93f5e-145">Contém uma coleção de elementos StyleSheet para o documento.</span><span class="sxs-lookup"><span data-stu-id="93f5e-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="93f5e-146">Atributos</span><span class="sxs-lookup"><span data-stu-id="93f5e-146">Attributes</span></span>

<span data-ttu-id="93f5e-147">Nenhum</span><span class="sxs-lookup"><span data-stu-id="93f5e-147">None.</span></span>
  

