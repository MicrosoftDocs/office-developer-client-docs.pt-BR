---
title: Windows_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: b8d8ed39637bdd692b2ba113525f40a3f91ffc9c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538435"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="f4044-102">Windows_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="f4044-102">Windows_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f4044-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="f4044-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4044-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f4044-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f4044-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f4044-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f4044-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f4044-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f4044-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="f4044-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f4044-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f4044-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f4044-109">Definição</span><span class="sxs-lookup"><span data-stu-id="f4044-109">Definition</span></span>

```XML
          <xs:complexType name="Windows_Type">
          
          <xs:sequence>
    <xs:element name="Window"  type="Window_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ClientWidth"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ClientHeight"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f4044-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f4044-110">Elements and attributes</span></span>

<span data-ttu-id="f4044-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f4044-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f4044-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f4044-112">Child elements</span></span>

|<span data-ttu-id="f4044-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f4044-113">**Element**</span></span>|<span data-ttu-id="f4044-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f4044-114">**Type**</span></span>|<span data-ttu-id="f4044-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f4044-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f4044-116">Janela</span><span class="sxs-lookup"><span data-stu-id="f4044-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f4044-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="f4044-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f4044-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="f4044-118">Attributes</span></span>

|<span data-ttu-id="f4044-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f4044-119">**Attribute**</span></span>|<span data-ttu-id="f4044-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f4044-120">**Type**</span></span>|<span data-ttu-id="f4044-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="f4044-121">**Required**</span></span>|<span data-ttu-id="f4044-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f4044-122">**Description**</span></span>|<span data-ttu-id="f4044-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="f4044-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f4044-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="f4044-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="f4044-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f4044-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f4044-126">opcional</span><span class="sxs-lookup"><span data-stu-id="f4044-126">optional</span></span>  <br/> ||<span data-ttu-id="f4044-127">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f4044-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f4044-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="f4044-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="f4044-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f4044-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f4044-130">opcional</span><span class="sxs-lookup"><span data-stu-id="f4044-130">optional</span></span>  <br/> ||<span data-ttu-id="f4044-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f4044-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

