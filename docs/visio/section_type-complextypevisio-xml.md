---
title: Section_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f8e855f-064c-d286-560f-9f89e7fce7b7
ms.openlocfilehash: 35cd638d36f4ddd1d90e0c312e65626f7d8b0bff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326093"
---
# <a name="sectiontype-complextype-visio-xml"></a><span data-ttu-id="adabb-102">Section_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="adabb-102">Section_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="adabb-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="adabb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="adabb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="adabb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="adabb-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="adabb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="adabb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="adabb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="adabb-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="adabb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="adabb-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="adabb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="adabb-109">Definição</span><span class="sxs-lookup"><span data-stu-id="adabb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="adabb-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="adabb-110">Elements and attributes</span></span>

<span data-ttu-id="adabb-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="adabb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="adabb-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="adabb-112">Child elements</span></span>

|<span data-ttu-id="adabb-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="adabb-113">**Element**</span></span>|<span data-ttu-id="adabb-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="adabb-114">**Type**</span></span>|<span data-ttu-id="adabb-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="adabb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="adabb-116">Cell</span><span class="sxs-lookup"><span data-stu-id="adabb-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="adabb-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="adabb-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="adabb-118">Linha</span><span class="sxs-lookup"><span data-stu-id="adabb-118">Row</span></span>](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[<span data-ttu-id="adabb-119">Row_Type</span><span class="sxs-lookup"><span data-stu-id="adabb-119">Row_Type</span></span>](row_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="adabb-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="adabb-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="adabb-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="adabb-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="adabb-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="adabb-122">Attributes</span></span>

|<span data-ttu-id="adabb-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="adabb-123">**Attribute**</span></span>|<span data-ttu-id="adabb-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="adabb-124">**Type**</span></span>|<span data-ttu-id="adabb-125">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="adabb-125">**Required**</span></span>|<span data-ttu-id="adabb-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="adabb-126">**Description**</span></span>|<span data-ttu-id="adabb-127">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="adabb-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="adabb-128">Del</span><span class="sxs-lookup"><span data-stu-id="adabb-128">Del</span></span>  <br/> |<span data-ttu-id="adabb-129">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="adabb-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="adabb-130">opcional</span><span class="sxs-lookup"><span data-stu-id="adabb-130">optional</span></span>  <br/> ||<span data-ttu-id="adabb-131">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="adabb-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="adabb-132">IX</span><span class="sxs-lookup"><span data-stu-id="adabb-132">IX</span></span>  <br/> |<span data-ttu-id="adabb-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="adabb-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="adabb-134">opcional</span><span class="sxs-lookup"><span data-stu-id="adabb-134">optional</span></span>  <br/> ||<span data-ttu-id="adabb-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="adabb-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="adabb-136">N</span><span class="sxs-lookup"><span data-stu-id="adabb-136">N</span></span>  <br/> |<span data-ttu-id="adabb-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="adabb-137">xsd:string</span></span>  <br/> |<span data-ttu-id="adabb-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="adabb-138">required</span></span>  <br/> ||<span data-ttu-id="adabb-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="adabb-139">Values of the xsd:string type.</span></span>  <br/> |
   

