---
title: FooterMargin_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: 69f5ce201bd1859aa716e0967939f0c1e5a5a2c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346043"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="92797-102">FooterMargin_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="92797-102">FooterMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="92797-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="92797-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92797-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="92797-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="92797-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="92797-105">**Schema file**</span></span> <br/> |<span data-ttu-id="92797-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="92797-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="92797-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="92797-107">**Extension base**</span></span> <br/> |<span data-ttu-id="92797-108">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="92797-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="92797-109">Definição</span><span class="sxs-lookup"><span data-stu-id="92797-109">Definition</span></span>

```XML
      <xs:complexType name="FooterMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="92797-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="92797-110">Elements and attributes</span></span>

<span data-ttu-id="92797-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="92797-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="92797-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="92797-112">Child elements</span></span>

<span data-ttu-id="92797-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="92797-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92797-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="92797-114">Attributes</span></span>

|<span data-ttu-id="92797-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="92797-115">**Attribute**</span></span>|<span data-ttu-id="92797-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="92797-116">**Type**</span></span>|<span data-ttu-id="92797-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="92797-117">**Required**</span></span>|<span data-ttu-id="92797-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="92797-118">**Description**</span></span>|<span data-ttu-id="92797-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="92797-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="92797-120">Unit</span><span class="sxs-lookup"><span data-stu-id="92797-120">Unit</span></span>  <br/> |<span data-ttu-id="92797-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="92797-121">xsd:string</span></span>  <br/> |<span data-ttu-id="92797-122">opcional</span><span class="sxs-lookup"><span data-stu-id="92797-122">optional</span></span>  <br/> ||<span data-ttu-id="92797-123">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="92797-123">Values of the xsd:string type.</span></span>  <br/> |
   

