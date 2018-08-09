---
title: Elemento VisioDocument ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: O elemento raiz de um documento do Microsoft Visio.
ms.openlocfilehash: 5a325b78ec64708246f0c8a6f5396c2ce1569121
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773279"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="7c2ea-103">Elemento VisioDocument ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="7c2ea-103">VisioDocument element ('Visio XML')</span></span>

<span data-ttu-id="7c2ea-104">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7c2ea-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="7c2ea-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c2ea-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7c2ea-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7c2ea-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="7c2ea-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7c2ea-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7c2ea-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7c2ea-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7c2ea-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7c2ea-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7c2ea-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7c2ea-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="7c2ea-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7c2ea-112">Document</span><span class="sxs-lookup"><span data-stu-id="7c2ea-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7c2ea-113">Definição</span><span class="sxs-lookup"><span data-stu-id="7c2ea-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7c2ea-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7c2ea-114">Elements and attributes</span></span>

<span data-ttu-id="7c2ea-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7c2ea-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7c2ea-116">Parent elements</span></span>

<span data-ttu-id="7c2ea-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7c2ea-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7c2ea-118">Child elements</span></span>

|<span data-ttu-id="7c2ea-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7c2ea-119">**Element**</span></span>|<span data-ttu-id="7c2ea-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7c2ea-120">**Type**</span></span>|<span data-ttu-id="7c2ea-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7c2ea-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7c2ea-122">Cores</span><span class="sxs-lookup"><span data-stu-id="7c2ea-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c2ea-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="7c2ea-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c2ea-124">Contém a tabela de cores do documento.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="7c2ea-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="7c2ea-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c2ea-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="7c2ea-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c2ea-127">Contém os elementos que especificam as configurações do documento.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="7c2ea-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="7c2ea-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c2ea-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="7c2ea-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c2ea-130">Especifica a estrutura do **ShapeSheet** de um documento.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="7c2ea-131">EventList</span><span class="sxs-lookup"><span data-stu-id="7c2ea-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c2ea-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="7c2ea-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c2ea-133">Contém um elemento **EventItem** para cada evento ao qual um objeto deve responder.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="7c2ea-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="7c2ea-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c2ea-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="7c2ea-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c2ea-136">Contém uma coleção de elementos de **FaceName** .</span><span class="sxs-lookup"><span data-stu-id="7c2ea-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="7c2ea-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="7c2ea-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c2ea-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="7c2ea-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c2ea-139">Contém os elementos de cabeçalho e rodapé de um documento.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="7c2ea-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="7c2ea-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c2ea-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="7c2ea-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c2ea-142">Especifica o conjunto de páginas que estão visíveis e está definida de recordsets são atualizáveis em um desenho de desenho.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="7c2ea-143">Folhas de estilo</span><span class="sxs-lookup"><span data-stu-id="7c2ea-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c2ea-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="7c2ea-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c2ea-145">Contém uma coleção de elementos de folha de estilos do documento.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7c2ea-146">Atributos</span><span class="sxs-lookup"><span data-stu-id="7c2ea-146">Attributes</span></span>

<span data-ttu-id="7c2ea-147">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-147">None.</span></span>
  

