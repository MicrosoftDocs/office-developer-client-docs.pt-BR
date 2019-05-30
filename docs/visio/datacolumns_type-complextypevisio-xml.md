---
title: DataColumns_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: ffe0fbfeaf0b0b67386a6cadd1beb78058819d39
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541145"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="d6363-102">DataColumns_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="d6363-102">DataColumns_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d6363-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="d6363-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6363-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d6363-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d6363-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d6363-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d6363-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d6363-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d6363-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="d6363-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d6363-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d6363-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d6363-109">Definição</span><span class="sxs-lookup"><span data-stu-id="d6363-109">Definition</span></span>

```XML
          <xs:complexType name="DataColumns_Type">
          
          <xs:sequence>
    <xs:element name="DataColumn"  type="DataColumn_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="SortColumn"
  type="xsd:string"
    />
    <xs:attribute name="SortAsc"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d6363-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d6363-110">Elements and attributes</span></span>

<span data-ttu-id="d6363-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d6363-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d6363-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d6363-112">Child elements</span></span>

|<span data-ttu-id="d6363-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d6363-113">**Element**</span></span>|<span data-ttu-id="d6363-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d6363-114">**Type**</span></span>|<span data-ttu-id="d6363-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d6363-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d6363-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="d6363-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d6363-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="d6363-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d6363-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="d6363-118">Attributes</span></span>

|<span data-ttu-id="d6363-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="d6363-119">**Attribute**</span></span>|<span data-ttu-id="d6363-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d6363-120">**Type**</span></span>|<span data-ttu-id="d6363-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="d6363-121">**Required**</span></span>|<span data-ttu-id="d6363-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d6363-122">**Description**</span></span>|<span data-ttu-id="d6363-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="d6363-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d6363-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="d6363-124">SortAsc</span></span>  <br/> |<span data-ttu-id="d6363-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="d6363-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d6363-126">opcional</span><span class="sxs-lookup"><span data-stu-id="d6363-126">optional</span></span>  <br/> ||<span data-ttu-id="d6363-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d6363-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d6363-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="d6363-128">SortColumn</span></span>  <br/> |<span data-ttu-id="d6363-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d6363-129">xsd:string</span></span>  <br/> |<span data-ttu-id="d6363-130">opcional</span><span class="sxs-lookup"><span data-stu-id="d6363-130">optional</span></span>  <br/> ||<span data-ttu-id="d6363-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d6363-131">Values of the xsd:string type.</span></span>  <br/> |
   

