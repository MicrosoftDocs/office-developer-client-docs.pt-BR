---
title: HeaderMargin_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 756b87f6-aa0e-c643-c733-7db788f63ac8
ms.openlocfilehash: 2d4a1fb15172d86a7843616679df4177d6f8292b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539086"
---
# <a name="headermargintype-complextype-visio-xml"></a><span data-ttu-id="3ccd6-102">HeaderMargin_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="3ccd6-102">HeaderMargin_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="3ccd6-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="3ccd6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ccd6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3ccd6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3ccd6-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3ccd6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3ccd6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3ccd6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3ccd6-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="3ccd6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3ccd6-108">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="3ccd6-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3ccd6-109">Definição</span><span class="sxs-lookup"><span data-stu-id="3ccd6-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3ccd6-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="3ccd6-110">Elements and attributes</span></span>

<span data-ttu-id="3ccd6-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3ccd6-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3ccd6-112">Child elements</span></span>

<span data-ttu-id="3ccd6-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ccd6-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="3ccd6-114">Attributes</span></span>

|<span data-ttu-id="3ccd6-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="3ccd6-115">**Attribute**</span></span>|<span data-ttu-id="3ccd6-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3ccd6-116">**Type**</span></span>|<span data-ttu-id="3ccd6-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="3ccd6-117">**Required**</span></span>|<span data-ttu-id="3ccd6-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3ccd6-118">**Description**</span></span>|<span data-ttu-id="3ccd6-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="3ccd6-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3ccd6-120">Une</span><span class="sxs-lookup"><span data-stu-id="3ccd6-120">Unit</span></span>  <br/> |<span data-ttu-id="3ccd6-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3ccd6-121">xsd:string</span></span>  <br/> |<span data-ttu-id="3ccd6-122">opcional</span><span class="sxs-lookup"><span data-stu-id="3ccd6-122">optional</span></span>  <br/> ||<span data-ttu-id="3ccd6-123">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-123">Values of the xsd:string type.</span></span>  <br/> |
   

