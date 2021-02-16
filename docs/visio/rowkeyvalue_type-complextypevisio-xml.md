---
title: RowKeyValue_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: e629a3a38927b7497d8d4f50299dc6be1b51c37b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541719"
---
# <a name="rowkeyvalue_type-complextype-visio-xml"></a><span data-ttu-id="1cb5f-102">RowKeyValue_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="1cb5f-102">RowKeyValue_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1cb5f-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="1cb5f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1cb5f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1cb5f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1cb5f-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1cb5f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1cb5f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1cb5f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1cb5f-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="1cb5f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1cb5f-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1cb5f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1cb5f-109">Definição</span><span class="sxs-lookup"><span data-stu-id="1cb5f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1cb5f-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1cb5f-110">Elements and attributes</span></span>

<span data-ttu-id="1cb5f-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1cb5f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1cb5f-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1cb5f-112">Child elements</span></span>

<span data-ttu-id="1cb5f-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1cb5f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1cb5f-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="1cb5f-114">Attributes</span></span>

|<span data-ttu-id="1cb5f-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1cb5f-115">**Attribute**</span></span>|<span data-ttu-id="1cb5f-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1cb5f-116">**Type**</span></span>|<span data-ttu-id="1cb5f-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="1cb5f-117">**Required**</span></span>|<span data-ttu-id="1cb5f-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1cb5f-118">**Description**</span></span>|<span data-ttu-id="1cb5f-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="1cb5f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1cb5f-120">RowID</span><span class="sxs-lookup"><span data-stu-id="1cb5f-120">RowID</span></span>  <br/> |<span data-ttu-id="1cb5f-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1cb5f-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1cb5f-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="1cb5f-122">required</span></span>  <br/> ||<span data-ttu-id="1cb5f-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1cb5f-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1cb5f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1cb5f-124">Value</span></span>  <br/> |<span data-ttu-id="1cb5f-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1cb5f-125">xsd:string</span></span>  <br/> |<span data-ttu-id="1cb5f-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="1cb5f-126">required</span></span>  <br/> ||<span data-ttu-id="1cb5f-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1cb5f-127">Values of the xsd:string type.</span></span>  <br/> |
   

