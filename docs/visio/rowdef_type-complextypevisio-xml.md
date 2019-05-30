---
title: RowDef_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64897258-dd7e-a730-d4f5-d9c217308491
ms.openlocfilehash: 79a01d9fe5edf1de933f05683eca3bfd6e95e4b3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538134"
---
# <a name="rowdeftype-complextype-visio-xml"></a><span data-ttu-id="212e3-102">RowDef_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="212e3-102">RowDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="212e3-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="212e3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="212e3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="212e3-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="212e3-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="212e3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="212e3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="212e3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="212e3-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="212e3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="212e3-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="212e3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="212e3-109">Definição</span><span class="sxs-lookup"><span data-stu-id="212e3-109">Definition</span></span>

```XML
          <xs:complexType name="RowDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="212e3-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="212e3-110">Elements and attributes</span></span>

<span data-ttu-id="212e3-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="212e3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="212e3-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="212e3-112">Child elements</span></span>

|<span data-ttu-id="212e3-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="212e3-113">**Element**</span></span>|<span data-ttu-id="212e3-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="212e3-114">**Type**</span></span>|<span data-ttu-id="212e3-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="212e3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="212e3-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="212e3-116">CellDef</span></span> <br/> |[<span data-ttu-id="212e3-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="212e3-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="212e3-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="212e3-118">Attributes</span></span>

<span data-ttu-id="212e3-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="212e3-119">None.</span></span>
  

