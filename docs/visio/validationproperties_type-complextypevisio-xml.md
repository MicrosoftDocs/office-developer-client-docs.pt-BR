---
title: ValidationProperties_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: d83a1ce8e7ad89155726200de2950da755e5d3db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538512"
---
# <a name="validationproperties_type-complextype-visio-xml"></a><span data-ttu-id="4f0a0-102">ValidationProperties_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="4f0a0-102">ValidationProperties_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="4f0a0-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="4f0a0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f0a0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4f0a0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4f0a0-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4f0a0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4f0a0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4f0a0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4f0a0-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="4f0a0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4f0a0-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4f0a0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4f0a0-109">Definição</span><span class="sxs-lookup"><span data-stu-id="4f0a0-109">Definition</span></span>

```XML
      <xs:complexType name="ValidationProperties_Type">
    <xs:attribute name="LastValidated"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="ShowIgnored"
  type="xsd:boolean"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4f0a0-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4f0a0-110">Elements and attributes</span></span>

<span data-ttu-id="4f0a0-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4f0a0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4f0a0-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4f0a0-112">Child elements</span></span>

<span data-ttu-id="4f0a0-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4f0a0-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f0a0-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="4f0a0-114">Attributes</span></span>

|<span data-ttu-id="4f0a0-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4f0a0-115">**Attribute**</span></span>|<span data-ttu-id="4f0a0-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4f0a0-116">**Type**</span></span>|<span data-ttu-id="4f0a0-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="4f0a0-117">**Required**</span></span>|<span data-ttu-id="4f0a0-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4f0a0-118">**Description**</span></span>|<span data-ttu-id="4f0a0-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="4f0a0-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4f0a0-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="4f0a0-120">LastValidated</span></span>  <br/> |<span data-ttu-id="4f0a0-121">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="4f0a0-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="4f0a0-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="4f0a0-122">required</span></span>  <br/> ||<span data-ttu-id="4f0a0-123">Valores do tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="4f0a0-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="4f0a0-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="4f0a0-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="4f0a0-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="4f0a0-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4f0a0-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="4f0a0-126">required</span></span>  <br/> ||<span data-ttu-id="4f0a0-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="4f0a0-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

