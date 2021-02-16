---
title: PrimaryKey_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 2e8b1a8238133bf579dadf80363a70be949f48d2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538792"
---
# <a name="primarykey_type-complextype-visio-xml"></a><span data-ttu-id="ffba1-102">PrimaryKey_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="ffba1-102">PrimaryKey_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ffba1-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="ffba1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffba1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ffba1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ffba1-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ffba1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ffba1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ffba1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ffba1-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="ffba1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ffba1-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ffba1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ffba1-109">Definição</span><span class="sxs-lookup"><span data-stu-id="ffba1-109">Definition</span></span>

```XML
          <xs:complexType name="PrimaryKey_Type">
          
          <xs:sequence>
    <xs:element name="RowKeyValue"  type="RowKeyValue_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ffba1-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ffba1-110">Elements and attributes</span></span>

<span data-ttu-id="ffba1-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ffba1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ffba1-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ffba1-112">Child elements</span></span>

|<span data-ttu-id="ffba1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ffba1-113">**Element**</span></span>|<span data-ttu-id="ffba1-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ffba1-114">**Type**</span></span>|<span data-ttu-id="ffba1-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ffba1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ffba1-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="ffba1-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ffba1-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="ffba1-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ffba1-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="ffba1-118">Attributes</span></span>

|<span data-ttu-id="ffba1-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ffba1-119">**Attribute**</span></span>|<span data-ttu-id="ffba1-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ffba1-120">**Type**</span></span>|<span data-ttu-id="ffba1-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="ffba1-121">**Required**</span></span>|<span data-ttu-id="ffba1-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ffba1-122">**Description**</span></span>|<span data-ttu-id="ffba1-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="ffba1-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ffba1-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="ffba1-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="ffba1-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ffba1-125">xsd:string</span></span>  <br/> |<span data-ttu-id="ffba1-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ffba1-126">required</span></span>  <br/> ||<span data-ttu-id="ffba1-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ffba1-127">Values of the xsd:string type.</span></span>  <br/> |
   

