---
title: Elemento VisioDocument ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: O elemento raiz de um documento do Microsoft Visio.
ms.openlocfilehash: 9829fa8960d78777e0fff4306b96978da90a647d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391301"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="45417-103">Elemento VisioDocument ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="45417-103">VisioDocument element ('Visio XML')</span></span>

<span data-ttu-id="45417-104">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="45417-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="45417-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="45417-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45417-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="45417-106">**Element type**</span></span> <br/> |[<span data-ttu-id="45417-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="45417-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="45417-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="45417-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="45417-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="45417-109">**Schema file**</span></span> <br/> |<span data-ttu-id="45417-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="45417-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="45417-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="45417-111">**Document parts**</span></span> <br/> |<span data-ttu-id="45417-112">Document</span><span class="sxs-lookup"><span data-stu-id="45417-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="45417-113">Definição</span><span class="sxs-lookup"><span data-stu-id="45417-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="45417-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="45417-114">Elements and attributes</span></span>

<span data-ttu-id="45417-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="45417-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="45417-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="45417-116">Parent elements</span></span>

<span data-ttu-id="45417-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="45417-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="45417-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="45417-118">Child elements</span></span>

|<span data-ttu-id="45417-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="45417-119">**Element**</span></span>|<span data-ttu-id="45417-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="45417-120">**Type**</span></span>|<span data-ttu-id="45417-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="45417-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="45417-122">Cores</span><span class="sxs-lookup"><span data-stu-id="45417-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45417-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="45417-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="45417-124">Contém a tabela de cores do documento.</span><span class="sxs-lookup"><span data-stu-id="45417-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="45417-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="45417-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45417-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="45417-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="45417-127">Contém os elementos que especificam as configurações do documento.</span><span class="sxs-lookup"><span data-stu-id="45417-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="45417-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="45417-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45417-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="45417-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="45417-130">Especifica a estrutura do **ShapeSheet** de um documento.</span><span class="sxs-lookup"><span data-stu-id="45417-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="45417-131">EventList</span><span class="sxs-lookup"><span data-stu-id="45417-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45417-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="45417-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="45417-133">Contém um elemento **EventItem** para cada evento ao qual um objeto deve responder.</span><span class="sxs-lookup"><span data-stu-id="45417-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="45417-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="45417-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45417-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="45417-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="45417-136">Contém uma coleção de elementos de **FaceName** .</span><span class="sxs-lookup"><span data-stu-id="45417-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="45417-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="45417-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45417-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="45417-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="45417-139">Contém os elementos de cabeçalho e rodapé de um documento.</span><span class="sxs-lookup"><span data-stu-id="45417-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="45417-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="45417-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45417-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="45417-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="45417-142">Especifica o conjunto de páginas que estão visíveis e está definida de recordsets são atualizáveis em um desenho de desenho.</span><span class="sxs-lookup"><span data-stu-id="45417-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="45417-143">Folhas de estilo</span><span class="sxs-lookup"><span data-stu-id="45417-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45417-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="45417-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="45417-145">Contém uma coleção de elementos de folha de estilos do documento.</span><span class="sxs-lookup"><span data-stu-id="45417-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="45417-146">Atributos</span><span class="sxs-lookup"><span data-stu-id="45417-146">Attributes</span></span>

<span data-ttu-id="45417-147">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="45417-147">None.</span></span>
  

