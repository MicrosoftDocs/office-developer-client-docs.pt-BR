---
title: FooterMargin_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: f5838855a5c21b699c7a81849b9afc40790f3d01
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538638"
---
# <a name="footermargin_type-complextype-visio-xml"></a><span data-ttu-id="d84dd-102">FooterMargin_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="d84dd-102">FooterMargin_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d84dd-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="d84dd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d84dd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d84dd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d84dd-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d84dd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d84dd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d84dd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d84dd-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="d84dd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d84dd-108">xsd:double</span><span class="sxs-lookup"><span data-stu-id="d84dd-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d84dd-109">Definição</span><span class="sxs-lookup"><span data-stu-id="d84dd-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d84dd-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d84dd-110">Elements and attributes</span></span>

<span data-ttu-id="d84dd-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d84dd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d84dd-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d84dd-112">Child elements</span></span>

<span data-ttu-id="d84dd-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d84dd-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d84dd-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="d84dd-114">Attributes</span></span>

|<span data-ttu-id="d84dd-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="d84dd-115">**Attribute**</span></span>|<span data-ttu-id="d84dd-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d84dd-116">**Type**</span></span>|<span data-ttu-id="d84dd-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="d84dd-117">**Required**</span></span>|<span data-ttu-id="d84dd-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d84dd-118">**Description**</span></span>|<span data-ttu-id="d84dd-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="d84dd-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d84dd-120">Unidade</span><span class="sxs-lookup"><span data-stu-id="d84dd-120">Unit</span></span>  <br/> |<span data-ttu-id="d84dd-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d84dd-121">xsd:string</span></span>  <br/> |<span data-ttu-id="d84dd-122">opcional</span><span class="sxs-lookup"><span data-stu-id="d84dd-122">optional</span></span>  <br/> ||<span data-ttu-id="d84dd-123">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d84dd-123">Values of the xsd:string type.</span></span>  <br/> |
   

