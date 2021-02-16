---
title: Elemento HeaderMargin (HeaderFooter_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2bb0f4c5-eacf-e09b-2fce-dcff2d927557
description: Especifica a margem do header de um documento.
ms.openlocfilehash: b7c055e818c490399df66e3e7ba626afc9645851
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539124"
---
# <a name="headermargin-element-headerfooter_type-complextype-visio-xml"></a><span data-ttu-id="43226-103">Elemento HeaderMargin (HeaderFooter_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="43226-103">HeaderMargin element (HeaderFooter_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="43226-104">Especifica a margem do header de um documento.</span><span class="sxs-lookup"><span data-stu-id="43226-104">Specifies the margin of a document's header.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43226-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="43226-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43226-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="43226-106">**Element type**</span></span> <br/> |[<span data-ttu-id="43226-107">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="43226-107">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="43226-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="43226-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="43226-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="43226-109">**Schema file**</span></span> <br/> |<span data-ttu-id="43226-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="43226-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="43226-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="43226-111">**Document parts**</span></span> <br/> |<span data-ttu-id="43226-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="43226-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="43226-113">Definição</span><span class="sxs-lookup"><span data-stu-id="43226-113">Definition</span></span>

```XML
< xs:element name="HeaderMargin" type="HeaderMargin_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="43226-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="43226-114">Elements and attributes</span></span>

<span data-ttu-id="43226-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="43226-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="43226-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="43226-116">Parent elements</span></span>

|<span data-ttu-id="43226-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="43226-117">**Element**</span></span>|<span data-ttu-id="43226-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="43226-118">**Type**</span></span>|<span data-ttu-id="43226-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="43226-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="43226-120">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="43226-120">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="43226-121">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="43226-121">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="43226-122">Contém elementos para o rodapé e o rodapé de um documento.</span><span class="sxs-lookup"><span data-stu-id="43226-122">Contains elements for a document's header and footer.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="43226-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="43226-123">Child elements</span></span>

<span data-ttu-id="43226-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="43226-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43226-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="43226-125">Attributes</span></span>

|<span data-ttu-id="43226-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="43226-126">**Attribute**</span></span>|<span data-ttu-id="43226-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="43226-127">**Type**</span></span>|<span data-ttu-id="43226-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="43226-128">**Required**</span></span>|<span data-ttu-id="43226-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="43226-129">**Description**</span></span>|<span data-ttu-id="43226-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="43226-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="43226-131">Unidade</span><span class="sxs-lookup"><span data-stu-id="43226-131">Unit</span></span>  <br/> |<span data-ttu-id="43226-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="43226-132">xsd:string</span></span>  <br/> |<span data-ttu-id="43226-133">opcional</span><span class="sxs-lookup"><span data-stu-id="43226-133">optional</span></span>  <br/> |<span data-ttu-id="43226-134">Representa uma unidade de medida.</span><span class="sxs-lookup"><span data-stu-id="43226-134">Represents a unit of measure.</span></span> <span data-ttu-id="43226-135">O padrão é DP.</span><span class="sxs-lookup"><span data-stu-id="43226-135">The default is DP.</span></span>  <br/> |<span data-ttu-id="43226-136">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="43226-136">Values of the xsd:string type.</span></span>  <br/> |
   

