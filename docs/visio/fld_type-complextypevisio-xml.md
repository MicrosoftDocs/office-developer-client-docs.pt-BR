---
title: fld_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: 2b1ecb21090658e1d2b042ac0f7e394d929d43c1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346204"
---
# <a name="fldtype-complextype-visio-xml"></a><span data-ttu-id="47c3b-102">fld_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="47c3b-102">fld_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="47c3b-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="47c3b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47c3b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="47c3b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="47c3b-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="47c3b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="47c3b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="47c3b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="47c3b-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="47c3b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="47c3b-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="47c3b-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="47c3b-109">Definição</span><span class="sxs-lookup"><span data-stu-id="47c3b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="47c3b-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="47c3b-110">Elements and attributes</span></span>

<span data-ttu-id="47c3b-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="47c3b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="47c3b-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="47c3b-112">Child elements</span></span>

<span data-ttu-id="47c3b-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="47c3b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47c3b-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="47c3b-114">Attributes</span></span>

|<span data-ttu-id="47c3b-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="47c3b-115">**Attribute**</span></span>|<span data-ttu-id="47c3b-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="47c3b-116">**Type**</span></span>|<span data-ttu-id="47c3b-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="47c3b-117">**Required**</span></span>|<span data-ttu-id="47c3b-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="47c3b-118">**Description**</span></span>|<span data-ttu-id="47c3b-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="47c3b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="47c3b-120">IX</span><span class="sxs-lookup"><span data-stu-id="47c3b-120">IX</span></span>  <br/> |<span data-ttu-id="47c3b-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="47c3b-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="47c3b-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="47c3b-122">required</span></span>  <br/> ||<span data-ttu-id="47c3b-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="47c3b-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

