---
title: HeaderMargin_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 756b87f6-aa0e-c643-c733-7db788f63ac8
ms.openlocfilehash: 9bb32471f1384c89e02e9ffdbcceebfc48d2b22e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330048"
---
# <a name="headermargintype-complextype-visio-xml"></a><span data-ttu-id="a2157-102">HeaderMargin_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a2157-102">HeaderMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a2157-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="a2157-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2157-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a2157-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a2157-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a2157-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a2157-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a2157-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a2157-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="a2157-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a2157-108">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="a2157-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a2157-109">Definição</span><span class="sxs-lookup"><span data-stu-id="a2157-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a2157-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="a2157-110">Elements and attributes</span></span>

<span data-ttu-id="a2157-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="a2157-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a2157-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a2157-112">Child elements</span></span>

<span data-ttu-id="a2157-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a2157-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a2157-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="a2157-114">Attributes</span></span>

|<span data-ttu-id="a2157-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a2157-115">**Attribute**</span></span>|<span data-ttu-id="a2157-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a2157-116">**Type**</span></span>|<span data-ttu-id="a2157-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="a2157-117">**Required**</span></span>|<span data-ttu-id="a2157-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a2157-118">**Description**</span></span>|<span data-ttu-id="a2157-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="a2157-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a2157-120">Unit</span><span class="sxs-lookup"><span data-stu-id="a2157-120">Unit</span></span>  <br/> |<span data-ttu-id="a2157-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a2157-121">xsd:string</span></span>  <br/> |<span data-ttu-id="a2157-122">opcional</span><span class="sxs-lookup"><span data-stu-id="a2157-122">optional</span></span>  <br/> ||<span data-ttu-id="a2157-123">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a2157-123">Values of the xsd:string type.</span></span>  <br/> |
   

