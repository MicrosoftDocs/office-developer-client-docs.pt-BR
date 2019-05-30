---
title: Trigger_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: 53a9efabe698e6b9c98c0471b97551c8ea2406da
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541894"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="87941-102">Trigger_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="87941-102">Trigger_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="87941-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="87941-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87941-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="87941-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="87941-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="87941-105">**Schema file**</span></span> <br/> |<span data-ttu-id="87941-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="87941-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="87941-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="87941-107">**Extension base**</span></span> <br/> |<span data-ttu-id="87941-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="87941-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="87941-109">Definição</span><span class="sxs-lookup"><span data-stu-id="87941-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="87941-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="87941-110">Elements and attributes</span></span>

<span data-ttu-id="87941-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="87941-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="87941-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="87941-112">Child elements</span></span>

|<span data-ttu-id="87941-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="87941-113">**Element**</span></span>|<span data-ttu-id="87941-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="87941-114">**Type**</span></span>|<span data-ttu-id="87941-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="87941-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="87941-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="87941-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="87941-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="87941-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="87941-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="87941-118">Attributes</span></span>

|<span data-ttu-id="87941-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="87941-119">**Attribute**</span></span>|<span data-ttu-id="87941-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="87941-120">**Type**</span></span>|<span data-ttu-id="87941-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="87941-121">**Required**</span></span>|<span data-ttu-id="87941-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="87941-122">**Description**</span></span>|<span data-ttu-id="87941-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="87941-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="87941-124">N</span><span class="sxs-lookup"><span data-stu-id="87941-124">N</span></span>  <br/> |<span data-ttu-id="87941-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="87941-125">xsd:string</span></span>  <br/> |<span data-ttu-id="87941-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="87941-126">required</span></span>  <br/> ||<span data-ttu-id="87941-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="87941-127">Values of the xsd:string type.</span></span>  <br/> |
   

