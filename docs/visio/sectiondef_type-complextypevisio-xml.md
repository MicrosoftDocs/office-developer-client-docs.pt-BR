---
title: SectionDef_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 96812d1911d249ebce02aeab20b0a77ef518fbff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542076"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="f99da-102">SectionDef_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="f99da-102">SectionDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f99da-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="f99da-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f99da-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f99da-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f99da-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f99da-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f99da-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f99da-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f99da-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="f99da-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f99da-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f99da-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f99da-109">Definição</span><span class="sxs-lookup"><span data-stu-id="f99da-109">Definition</span></span>

```XML
          <xs:complexType name="SectionDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowDef"  type="RowDef_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f99da-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f99da-110">Elements and attributes</span></span>

<span data-ttu-id="f99da-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f99da-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f99da-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f99da-112">Child elements</span></span>

|<span data-ttu-id="f99da-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f99da-113">**Element**</span></span>|<span data-ttu-id="f99da-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f99da-114">**Type**</span></span>|<span data-ttu-id="f99da-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f99da-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f99da-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="f99da-116">CellDef</span></span> <br/> |[<span data-ttu-id="f99da-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="f99da-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="f99da-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="f99da-118">RowDef</span></span> <br/> |[<span data-ttu-id="f99da-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="f99da-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f99da-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="f99da-120">Attributes</span></span>

|<span data-ttu-id="f99da-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f99da-121">**Attribute**</span></span>|<span data-ttu-id="f99da-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f99da-122">**Type**</span></span>|<span data-ttu-id="f99da-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="f99da-123">**Required**</span></span>|<span data-ttu-id="f99da-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f99da-124">**Description**</span></span>|<span data-ttu-id="f99da-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="f99da-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f99da-126">N</span><span class="sxs-lookup"><span data-stu-id="f99da-126">N</span></span>  <br/> |<span data-ttu-id="f99da-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f99da-127">xsd:string</span></span>  <br/> |<span data-ttu-id="f99da-128">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f99da-128">required</span></span>  <br/> ||<span data-ttu-id="f99da-129">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f99da-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f99da-130">S</span><span class="sxs-lookup"><span data-stu-id="f99da-130">S</span></span>  <br/> |<span data-ttu-id="f99da-131">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="f99da-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="f99da-132">opcional</span><span class="sxs-lookup"><span data-stu-id="f99da-132">optional</span></span>  <br/> ||<span data-ttu-id="f99da-133">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="f99da-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="f99da-134">E</span><span class="sxs-lookup"><span data-stu-id="f99da-134">T</span></span>  <br/> |<span data-ttu-id="f99da-135">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f99da-135">xsd:string</span></span>  <br/> |<span data-ttu-id="f99da-136">opcional</span><span class="sxs-lookup"><span data-stu-id="f99da-136">optional</span></span>  <br/> ||<span data-ttu-id="f99da-137">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f99da-137">Values of the xsd:string type.</span></span>  <br/> |
   

