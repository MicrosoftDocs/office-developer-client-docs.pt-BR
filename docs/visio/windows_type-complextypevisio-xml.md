---
title: Windows_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: 5aeffa7b78c4c402d03b6a2774a2df8b339e03e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346442"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="3a22a-102">Windows_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="3a22a-102">Windows_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3a22a-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="3a22a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a22a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3a22a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3a22a-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3a22a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3a22a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3a22a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3a22a-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="3a22a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3a22a-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3a22a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3a22a-109">Definição</span><span class="sxs-lookup"><span data-stu-id="3a22a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3a22a-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="3a22a-110">Elements and attributes</span></span>

<span data-ttu-id="3a22a-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="3a22a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3a22a-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3a22a-112">Child elements</span></span>

|<span data-ttu-id="3a22a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3a22a-113">**Element**</span></span>|<span data-ttu-id="3a22a-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3a22a-114">**Type**</span></span>|<span data-ttu-id="3a22a-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3a22a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3a22a-116">Janela</span><span class="sxs-lookup"><span data-stu-id="3a22a-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3a22a-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="3a22a-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3a22a-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="3a22a-118">Attributes</span></span>

|<span data-ttu-id="3a22a-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="3a22a-119">**Attribute**</span></span>|<span data-ttu-id="3a22a-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3a22a-120">**Type**</span></span>|<span data-ttu-id="3a22a-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="3a22a-121">**Required**</span></span>|<span data-ttu-id="3a22a-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3a22a-122">**Description**</span></span>|<span data-ttu-id="3a22a-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="3a22a-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3a22a-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="3a22a-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="3a22a-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="3a22a-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="3a22a-126">opcional</span><span class="sxs-lookup"><span data-stu-id="3a22a-126">optional</span></span>  <br/> ||<span data-ttu-id="3a22a-127">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="3a22a-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="3a22a-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="3a22a-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="3a22a-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="3a22a-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="3a22a-130">opcional</span><span class="sxs-lookup"><span data-stu-id="3a22a-130">optional</span></span>  <br/> ||<span data-ttu-id="3a22a-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="3a22a-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

