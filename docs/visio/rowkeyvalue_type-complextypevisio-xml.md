---
title: RowKeyValue_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: 512675538aa17415fa44684613dcd635fe23857f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332470"
---
# <a name="rowkeyvaluetype-complextype-visio-xml"></a><span data-ttu-id="361f4-102">RowKeyValue_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="361f4-102">RowKeyValue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="361f4-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="361f4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="361f4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="361f4-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="361f4-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="361f4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="361f4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="361f4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="361f4-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="361f4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="361f4-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="361f4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="361f4-109">Definição</span><span class="sxs-lookup"><span data-stu-id="361f4-109">Definition</span></span>

```XML
      <xs:complexType name="RowKeyValue_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Value"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="361f4-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="361f4-110">Elements and attributes</span></span>

<span data-ttu-id="361f4-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="361f4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="361f4-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="361f4-112">Child elements</span></span>

<span data-ttu-id="361f4-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="361f4-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="361f4-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="361f4-114">Attributes</span></span>

|<span data-ttu-id="361f4-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="361f4-115">**Attribute**</span></span>|<span data-ttu-id="361f4-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="361f4-116">**Type**</span></span>|<span data-ttu-id="361f4-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="361f4-117">**Required**</span></span>|<span data-ttu-id="361f4-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="361f4-118">**Description**</span></span>|<span data-ttu-id="361f4-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="361f4-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="361f4-120">RowID</span><span class="sxs-lookup"><span data-stu-id="361f4-120">RowID</span></span>  <br/> |<span data-ttu-id="361f4-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="361f4-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="361f4-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="361f4-122">required</span></span>  <br/> ||<span data-ttu-id="361f4-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="361f4-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="361f4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="361f4-124">Value</span></span>  <br/> |<span data-ttu-id="361f4-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="361f4-125">xsd:string</span></span>  <br/> |<span data-ttu-id="361f4-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="361f4-126">required</span></span>  <br/> ||<span data-ttu-id="361f4-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="361f4-127">Values of the xsd:string type.</span></span>  <br/> |
   

