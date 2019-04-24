---
title: Trigger_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: e34ef122a6f0a08168f838fdaeb130d68349ecb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280854"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="b4878-102">Trigger_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="b4878-102">Trigger_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b4878-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="b4878-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4878-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b4878-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b4878-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b4878-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b4878-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b4878-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b4878-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="b4878-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b4878-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b4878-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b4878-109">Definição</span><span class="sxs-lookup"><span data-stu-id="b4878-109">Definition</span></span>

```XML
          <xs:complexType name="Trigger_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b4878-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="b4878-110">Elements and attributes</span></span>

<span data-ttu-id="b4878-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="b4878-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b4878-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b4878-112">Child elements</span></span>

|<span data-ttu-id="b4878-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b4878-113">**Element**</span></span>|<span data-ttu-id="b4878-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b4878-114">**Type**</span></span>|<span data-ttu-id="b4878-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b4878-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b4878-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="b4878-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b4878-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="b4878-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b4878-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="b4878-118">Attributes</span></span>

|<span data-ttu-id="b4878-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b4878-119">**Attribute**</span></span>|<span data-ttu-id="b4878-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b4878-120">**Type**</span></span>|<span data-ttu-id="b4878-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="b4878-121">**Required**</span></span>|<span data-ttu-id="b4878-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b4878-122">**Description**</span></span>|<span data-ttu-id="b4878-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="b4878-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b4878-124">N</span><span class="sxs-lookup"><span data-stu-id="b4878-124">N</span></span>  <br/> |<span data-ttu-id="b4878-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b4878-125">xsd:string</span></span>  <br/> |<span data-ttu-id="b4878-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="b4878-126">required</span></span>  <br/> ||<span data-ttu-id="b4878-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b4878-127">Values of the xsd:string type.</span></span>  <br/> |
   

