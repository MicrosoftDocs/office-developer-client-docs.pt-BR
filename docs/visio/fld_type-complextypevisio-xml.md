---
title: fld_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: 5651a0b0a2d09e3fbbdb0d1dbf66f1be3d374c12
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539597"
---
# <a name="fld_type-complextype-visio-xml"></a><span data-ttu-id="ff09f-102">fld_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="ff09f-102">fld_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ff09f-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="ff09f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff09f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ff09f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ff09f-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ff09f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ff09f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ff09f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ff09f-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="ff09f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ff09f-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ff09f-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ff09f-109">Definição</span><span class="sxs-lookup"><span data-stu-id="ff09f-109">Definition</span></span>

```XML
      <xs:complexType name="fld_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ff09f-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ff09f-110">Elements and attributes</span></span>

<span data-ttu-id="ff09f-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ff09f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ff09f-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ff09f-112">Child elements</span></span>

<span data-ttu-id="ff09f-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ff09f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff09f-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="ff09f-114">Attributes</span></span>

|<span data-ttu-id="ff09f-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ff09f-115">**Attribute**</span></span>|<span data-ttu-id="ff09f-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ff09f-116">**Type**</span></span>|<span data-ttu-id="ff09f-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="ff09f-117">**Required**</span></span>|<span data-ttu-id="ff09f-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ff09f-118">**Description**</span></span>|<span data-ttu-id="ff09f-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="ff09f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ff09f-120">IX</span><span class="sxs-lookup"><span data-stu-id="ff09f-120">IX</span></span>  <br/> |<span data-ttu-id="ff09f-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff09f-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff09f-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ff09f-122">required</span></span>  <br/> ||<span data-ttu-id="ff09f-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ff09f-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

