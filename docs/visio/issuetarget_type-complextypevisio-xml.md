---
title: IssueTarget_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: d7b8309bb6dac9648d379c89687dc89165f44edf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314921"
---
# <a name="issuetargettype-complextype-visio-xml"></a><span data-ttu-id="7300b-102">IssueTarget_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="7300b-102">IssueTarget_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7300b-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="7300b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7300b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7300b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7300b-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7300b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7300b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7300b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7300b-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="7300b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7300b-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7300b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7300b-109">Definição</span><span class="sxs-lookup"><span data-stu-id="7300b-109">Definition</span></span>

```XML
      <xs:complexType name="IssueTarget_Type">
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7300b-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7300b-110">Elements and attributes</span></span>

<span data-ttu-id="7300b-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7300b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7300b-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7300b-112">Child elements</span></span>

<span data-ttu-id="7300b-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7300b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7300b-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="7300b-114">Attributes</span></span>

|<span data-ttu-id="7300b-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7300b-115">**Attribute**</span></span>|<span data-ttu-id="7300b-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7300b-116">**Type**</span></span>|<span data-ttu-id="7300b-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="7300b-117">**Required**</span></span>|<span data-ttu-id="7300b-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7300b-118">**Description**</span></span>|<span data-ttu-id="7300b-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="7300b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7300b-120">PageID</span><span class="sxs-lookup"><span data-stu-id="7300b-120">PageID</span></span>  <br/> |<span data-ttu-id="7300b-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7300b-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7300b-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="7300b-122">required</span></span>  <br/> ||<span data-ttu-id="7300b-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7300b-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7300b-124">ShapeID</span><span class="sxs-lookup"><span data-stu-id="7300b-124">ShapeID</span></span>  <br/> |<span data-ttu-id="7300b-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7300b-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7300b-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="7300b-126">required</span></span>  <br/> ||<span data-ttu-id="7300b-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7300b-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

