---
title: ActionTag_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bcc17e7-d59d-d392-f299-78d7665202fc
ms.openlocfilehash: a30290ee9dbb86c7af75820bd767bb95ce4add21
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384770"
---
# <a name="actiontagtype-complextype-visio-xml"></a><span data-ttu-id="99ccf-102">ActionTag_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="99ccf-102">ActionTag_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="99ccf-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="99ccf-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99ccf-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="99ccf-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="99ccf-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="99ccf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="99ccf-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="99ccf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="99ccf-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="99ccf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="99ccf-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="99ccf-108">Section_Type complexType</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="99ccf-109">Definição</span><span class="sxs-lookup"><span data-stu-id="99ccf-109">Definition</span></span>

```XML
          <xs:complexType name="ActionTag_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionTagRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="99ccf-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="99ccf-110">Elements and attributes</span></span>

<span data-ttu-id="99ccf-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="99ccf-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="99ccf-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="99ccf-112">Child elements</span></span>

|<span data-ttu-id="99ccf-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99ccf-113">**Element**</span></span>|<span data-ttu-id="99ccf-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="99ccf-114">**Type**</span></span>|<span data-ttu-id="99ccf-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="99ccf-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="99ccf-116">Linha</span><span class="sxs-lookup"><span data-stu-id="99ccf-116">Row</span></span>](row-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="99ccf-117">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="99ccf-117">ActionTagRow_Type complexType</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="99ccf-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="99ccf-118">Attributes</span></span>

<span data-ttu-id="99ccf-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="99ccf-119">None.</span></span>
  

