---
title: Section_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f8e855f-064c-d286-560f-9f89e7fce7b7
ms.openlocfilehash: 48dd7a0ffc487b4a7a4200505f08d0aca42fd3c6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542125"
---
# <a name="sectiontype-complextype-visio-xml"></a><span data-ttu-id="dfe20-102">Section_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="dfe20-102">Section_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="dfe20-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="dfe20-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dfe20-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dfe20-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="dfe20-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="dfe20-105">**Schema file**</span></span> <br/> |<span data-ttu-id="dfe20-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="dfe20-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="dfe20-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="dfe20-107">**Extension base**</span></span> <br/> |<span data-ttu-id="dfe20-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfe20-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dfe20-109">Definição</span><span class="sxs-lookup"><span data-stu-id="dfe20-109">Definition</span></span>

```XML
          <xs:complexType name="Section_Type">
          
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Trigger"  type="Trigger_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Row"  type="Row_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dfe20-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="dfe20-110">Elements and attributes</span></span>

<span data-ttu-id="dfe20-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="dfe20-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dfe20-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="dfe20-112">Child elements</span></span>

|<span data-ttu-id="dfe20-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dfe20-113">**Element**</span></span>|<span data-ttu-id="dfe20-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dfe20-114">**Type**</span></span>|<span data-ttu-id="dfe20-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dfe20-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dfe20-116">Cell</span><span class="sxs-lookup"><span data-stu-id="dfe20-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="dfe20-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="dfe20-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="dfe20-118">Linha</span><span class="sxs-lookup"><span data-stu-id="dfe20-118">Row</span></span>](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[<span data-ttu-id="dfe20-119">Row_Type</span><span class="sxs-lookup"><span data-stu-id="dfe20-119">Row_Type</span></span>](row_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="dfe20-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="dfe20-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="dfe20-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="dfe20-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="dfe20-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="dfe20-122">Attributes</span></span>

|<span data-ttu-id="dfe20-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="dfe20-123">**Attribute**</span></span>|<span data-ttu-id="dfe20-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dfe20-124">**Type**</span></span>|<span data-ttu-id="dfe20-125">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="dfe20-125">**Required**</span></span>|<span data-ttu-id="dfe20-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dfe20-126">**Description**</span></span>|<span data-ttu-id="dfe20-127">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="dfe20-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dfe20-128">Del</span><span class="sxs-lookup"><span data-stu-id="dfe20-128">Del</span></span>  <br/> |<span data-ttu-id="dfe20-129">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="dfe20-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="dfe20-130">opcional</span><span class="sxs-lookup"><span data-stu-id="dfe20-130">optional</span></span>  <br/> ||<span data-ttu-id="dfe20-131">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="dfe20-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="dfe20-132">IX</span><span class="sxs-lookup"><span data-stu-id="dfe20-132">IX</span></span>  <br/> |<span data-ttu-id="dfe20-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dfe20-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dfe20-134">opcional</span><span class="sxs-lookup"><span data-stu-id="dfe20-134">optional</span></span>  <br/> ||<span data-ttu-id="dfe20-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="dfe20-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dfe20-136">N</span><span class="sxs-lookup"><span data-stu-id="dfe20-136">N</span></span>  <br/> |<span data-ttu-id="dfe20-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dfe20-137">xsd:string</span></span>  <br/> |<span data-ttu-id="dfe20-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="dfe20-138">required</span></span>  <br/> ||<span data-ttu-id="dfe20-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="dfe20-139">Values of the xsd:string type.</span></span>  <br/> |
   

