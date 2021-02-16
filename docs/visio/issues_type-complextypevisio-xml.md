---
title: Issues_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f326e227-f68e-27d6-268e-1ae935516dbc
ms.openlocfilehash: 160afddb1352a93050496a9b3497a3e3b6f2e585
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538106"
---
# <a name="issues_type-complextype-visio-xml"></a><span data-ttu-id="8b0d4-102">Issues_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="8b0d4-102">Issues_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8b0d4-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="8b0d4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b0d4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8b0d4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8b0d4-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8b0d4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8b0d4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8b0d4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8b0d4-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="8b0d4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8b0d4-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8b0d4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8b0d4-109">Definição</span><span class="sxs-lookup"><span data-stu-id="8b0d4-109">Definition</span></span>

```XML
          <xs:complexType name="Issues_Type">
          
          <xs:sequence>
    <xs:element name="Issue"  type="Issue_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8b0d4-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="8b0d4-110">Elements and attributes</span></span>

<span data-ttu-id="8b0d4-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="8b0d4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8b0d4-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8b0d4-112">Child elements</span></span>

|<span data-ttu-id="8b0d4-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8b0d4-113">**Element**</span></span>|<span data-ttu-id="8b0d4-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8b0d4-114">**Type**</span></span>|<span data-ttu-id="8b0d4-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8b0d4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8b0d4-116">Problema</span><span class="sxs-lookup"><span data-stu-id="8b0d4-116">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8b0d4-117">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="8b0d4-117">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8b0d4-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="8b0d4-118">Attributes</span></span>

<span data-ttu-id="8b0d4-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8b0d4-119">None.</span></span>
  

