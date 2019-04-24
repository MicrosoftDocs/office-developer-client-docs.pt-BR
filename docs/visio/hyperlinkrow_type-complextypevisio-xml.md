---
title: HyperlinkRow_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f8ded1a6-3bbd-0d59-c9f0-ab84341888cd
ms.openlocfilehash: 0056c87f4926f440ffcfd85619fd5ab7cba308db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344829"
---
# <a name="hyperlinkrowtype-complextype-visio-xml"></a><span data-ttu-id="71311-102">HyperlinkRow_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="71311-102">HyperlinkRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="71311-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="71311-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71311-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="71311-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="71311-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="71311-105">**Schema file**</span></span> <br/> |<span data-ttu-id="71311-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="71311-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="71311-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="71311-107">**Extension base**</span></span> <br/> |<span data-ttu-id="71311-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="71311-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="71311-109">Definição</span><span class="sxs-lookup"><span data-stu-id="71311-109">Definition</span></span>

```XML
          <xs:complexType name="HyperlinkRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="71311-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="71311-110">Elements and attributes</span></span>

<span data-ttu-id="71311-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="71311-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="71311-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="71311-112">Child elements</span></span>

|<span data-ttu-id="71311-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="71311-113">**Element**</span></span>|<span data-ttu-id="71311-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="71311-114">**Type**</span></span>|<span data-ttu-id="71311-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="71311-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="71311-116">Cell</span><span class="sxs-lookup"><span data-stu-id="71311-116">Cell</span></span>](cell-element-hyperlink-rowvisio-xml.md) <br/> |[<span data-ttu-id="71311-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="71311-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="71311-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="71311-118">Attributes</span></span>

<span data-ttu-id="71311-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="71311-119">None.</span></span>
  

