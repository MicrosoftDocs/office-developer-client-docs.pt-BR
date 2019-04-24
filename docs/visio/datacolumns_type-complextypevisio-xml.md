---
title: DataColumns_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: 6d802bf646ee87f4c96b9ce041352af3cab48a16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344594"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="3b387-102">DataColumns_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="3b387-102">DataColumns_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3b387-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="3b387-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b387-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3b387-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3b387-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3b387-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3b387-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3b387-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3b387-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="3b387-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3b387-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3b387-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3b387-109">Definição</span><span class="sxs-lookup"><span data-stu-id="3b387-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3b387-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="3b387-110">Elements and attributes</span></span>

<span data-ttu-id="3b387-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="3b387-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3b387-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3b387-112">Child elements</span></span>

|<span data-ttu-id="3b387-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3b387-113">**Element**</span></span>|<span data-ttu-id="3b387-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3b387-114">**Type**</span></span>|<span data-ttu-id="3b387-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3b387-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3b387-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="3b387-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3b387-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="3b387-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3b387-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="3b387-118">Attributes</span></span>

|<span data-ttu-id="3b387-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="3b387-119">**Attribute**</span></span>|<span data-ttu-id="3b387-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3b387-120">**Type**</span></span>|<span data-ttu-id="3b387-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="3b387-121">**Required**</span></span>|<span data-ttu-id="3b387-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3b387-122">**Description**</span></span>|<span data-ttu-id="3b387-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="3b387-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3b387-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="3b387-124">SortAsc</span></span>  <br/> |<span data-ttu-id="3b387-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="3b387-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3b387-126">opcional</span><span class="sxs-lookup"><span data-stu-id="3b387-126">optional</span></span>  <br/> ||<span data-ttu-id="3b387-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="3b387-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3b387-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="3b387-128">SortColumn</span></span>  <br/> |<span data-ttu-id="3b387-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3b387-129">xsd:string</span></span>  <br/> |<span data-ttu-id="3b387-130">opcional</span><span class="sxs-lookup"><span data-stu-id="3b387-130">optional</span></span>  <br/> ||<span data-ttu-id="3b387-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3b387-131">Values of the xsd:string type.</span></span>  <br/> |
   

