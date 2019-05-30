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
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="4c576-102">ValidationProperties_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="4c576-102">ValidationProperties_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="4c576-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="4c576-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c576-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4c576-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4c576-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4c576-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4c576-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4c576-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4c576-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="4c576-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4c576-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4c576-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4c576-109">Definição</span><span class="sxs-lookup"><span data-stu-id="4c576-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4c576-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4c576-110">Elements and attributes</span></span>

<span data-ttu-id="4c576-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4c576-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4c576-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4c576-112">Child elements</span></span>

<span data-ttu-id="4c576-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4c576-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c576-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="4c576-114">Attributes</span></span>

|<span data-ttu-id="4c576-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4c576-115">**Attribute**</span></span>|<span data-ttu-id="4c576-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4c576-116">**Type**</span></span>|<span data-ttu-id="4c576-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="4c576-117">**Required**</span></span>|<span data-ttu-id="4c576-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4c576-118">**Description**</span></span>|<span data-ttu-id="4c576-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="4c576-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4c576-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="4c576-120">LastValidated</span></span>  <br/> |<span data-ttu-id="4c576-121">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="4c576-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="4c576-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="4c576-122">required</span></span>  <br/> ||<span data-ttu-id="4c576-123">Valores do tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="4c576-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="4c576-124">Não ignorado</span><span class="sxs-lookup"><span data-stu-id="4c576-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="4c576-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="4c576-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4c576-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="4c576-126">required</span></span>  <br/> ||<span data-ttu-id="4c576-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="4c576-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

