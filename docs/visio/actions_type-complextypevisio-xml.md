---
title: Actions_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31070969-2091-d00e-5dd1-b9c6034f76d9
ms.openlocfilehash: 384b948c61f3b618d108db090721ea6768d69372
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538407"
---
# <a name="actionstype-complextype-visio-xml"></a><span data-ttu-id="aabdd-102">Actions_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="aabdd-102">Actions_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="aabdd-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="aabdd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aabdd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aabdd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="aabdd-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="aabdd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="aabdd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="aabdd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="aabdd-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="aabdd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="aabdd-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="aabdd-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aabdd-109">Definição</span><span class="sxs-lookup"><span data-stu-id="aabdd-109">Definition</span></span>

```XML
          <xs:complexType name="Actions_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="aabdd-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="aabdd-110">Elements and attributes</span></span>

<span data-ttu-id="aabdd-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="aabdd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="aabdd-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="aabdd-112">Child elements</span></span>

|<span data-ttu-id="aabdd-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aabdd-113">**Element**</span></span>|<span data-ttu-id="aabdd-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="aabdd-114">**Type**</span></span>|<span data-ttu-id="aabdd-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aabdd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aabdd-116">Linha</span><span class="sxs-lookup"><span data-stu-id="aabdd-116">Row</span></span>](row-element-actions-sectionvisio-xml.md) <br/> |[<span data-ttu-id="aabdd-117">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="aabdd-117">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="aabdd-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="aabdd-118">Attributes</span></span>

<span data-ttu-id="aabdd-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="aabdd-119">None.</span></span>
  

