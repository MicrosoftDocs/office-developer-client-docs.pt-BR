---
title: Issues_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f326e227-f68e-27d6-268e-1ae935516dbc
ms.openlocfilehash: 42482db0c4542398381bc02ec5b21a8b80fac62f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397230"
---
# <a name="issuestype-complextype-visio-xml"></a><span data-ttu-id="30db1-102">Issues_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="30db1-102">Issues_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="30db1-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="30db1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30db1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="30db1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="30db1-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="30db1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="30db1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="30db1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="30db1-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="30db1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="30db1-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="30db1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="30db1-109">Definição</span><span class="sxs-lookup"><span data-stu-id="30db1-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="30db1-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="30db1-110">Elements and attributes</span></span>

<span data-ttu-id="30db1-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="30db1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="30db1-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="30db1-112">Child elements</span></span>

|<span data-ttu-id="30db1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="30db1-113">**Element**</span></span>|<span data-ttu-id="30db1-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="30db1-114">**Type**</span></span>|<span data-ttu-id="30db1-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="30db1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="30db1-116">Problema</span><span class="sxs-lookup"><span data-stu-id="30db1-116">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30db1-117">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="30db1-117">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="30db1-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="30db1-118">Attributes</span></span>

<span data-ttu-id="30db1-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="30db1-119">None.</span></span>
  

