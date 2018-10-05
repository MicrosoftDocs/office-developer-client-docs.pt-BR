---
title: User_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d3970d90-6beb-1f59-256f-ace6a9865b59
ms.openlocfilehash: 336a4769d48885eaa2e75a812541497714359e0c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382244"
---
# <a name="usertype-complextype-visio-xml"></a><span data-ttu-id="4dc3c-102">User_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="4dc3c-102">User_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4dc3c-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="4dc3c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4dc3c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4dc3c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4dc3c-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4dc3c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4dc3c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4dc3c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4dc3c-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="4dc3c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4dc3c-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="4dc3c-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4dc3c-109">Definição</span><span class="sxs-lookup"><span data-stu-id="4dc3c-109">Definition</span></span>

```XML
          <xs:complexType name="User_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="UserRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4dc3c-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4dc3c-110">Elements and attributes</span></span>

<span data-ttu-id="4dc3c-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4dc3c-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4dc3c-112">Child elements</span></span>

|<span data-ttu-id="4dc3c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4dc3c-113">**Element**</span></span>|<span data-ttu-id="4dc3c-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4dc3c-114">**Type**</span></span>|<span data-ttu-id="4dc3c-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4dc3c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4dc3c-116">Row</span><span class="sxs-lookup"><span data-stu-id="4dc3c-116">Row</span></span>](row-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="4dc3c-117">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="4dc3c-117">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4dc3c-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="4dc3c-118">Attributes</span></span>

<span data-ttu-id="4dc3c-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-119">None.</span></span>
  

