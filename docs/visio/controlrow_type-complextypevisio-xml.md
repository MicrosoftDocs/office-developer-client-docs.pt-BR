---
title: ControlRow_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f9ee251-e685-e56c-3c8a-cb727ad62064
ms.openlocfilehash: a6bd54f425e211716ce7dc9a7206a3d079383d5d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538666"
---
# <a name="controlrowtype-complextype-visio-xml"></a><span data-ttu-id="3ed12-102">ControlRow_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="3ed12-102">ControlRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="3ed12-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="3ed12-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ed12-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3ed12-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3ed12-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3ed12-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3ed12-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3ed12-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3ed12-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="3ed12-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3ed12-108">NamedIndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="3ed12-108">NamedIndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3ed12-109">Definição</span><span class="sxs-lookup"><span data-stu-id="3ed12-109">Definition</span></span>

```XML
          <xs:complexType name="ControlRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedIndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="3ed12-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="3ed12-110">Elements and attributes</span></span>

<span data-ttu-id="3ed12-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="3ed12-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3ed12-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3ed12-112">Child elements</span></span>

|<span data-ttu-id="3ed12-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3ed12-113">**Element**</span></span>|<span data-ttu-id="3ed12-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3ed12-114">**Type**</span></span>|<span data-ttu-id="3ed12-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3ed12-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3ed12-116">Cell</span><span class="sxs-lookup"><span data-stu-id="3ed12-116">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="3ed12-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="3ed12-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3ed12-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="3ed12-118">Attributes</span></span>

<span data-ttu-id="3ed12-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3ed12-119">None.</span></span>
  

