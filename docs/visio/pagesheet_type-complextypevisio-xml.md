---
title: PageSheet_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 70cd45ad803f9342b582f324b31f12ac5dff54c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772463"
---
# <a name="pagesheettype-complextype-visio-xml"></a><span data-ttu-id="287f7-102">PageSheet_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="287f7-102">PageSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="287f7-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="287f7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="287f7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="287f7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="287f7-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="287f7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="287f7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="287f7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="287f7-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="287f7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="287f7-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="287f7-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="287f7-109">Definição</span><span class="sxs-lookup"><span data-stu-id="287f7-109">Definition</span></span>

```XML
      <xs:complexType name="PageSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="287f7-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="287f7-110">Elements and attributes</span></span>

<span data-ttu-id="287f7-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="287f7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="287f7-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="287f7-112">Child elements</span></span>

<span data-ttu-id="287f7-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="287f7-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="287f7-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="287f7-114">Attributes</span></span>

|<span data-ttu-id="287f7-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="287f7-115">**Attribute**</span></span>|<span data-ttu-id="287f7-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="287f7-116">**Type**</span></span>|<span data-ttu-id="287f7-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="287f7-117">**Required**</span></span>|<span data-ttu-id="287f7-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="287f7-118">**Description**</span></span>|<span data-ttu-id="287f7-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="287f7-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="287f7-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="287f7-120">UniqueID</span></span>  <br/> |<span data-ttu-id="287f7-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="287f7-121">xsd:string</span></span>  <br/> |<span data-ttu-id="287f7-122">opcional</span><span class="sxs-lookup"><span data-stu-id="287f7-122">optional</span></span>  <br/> ||<span data-ttu-id="287f7-123">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="287f7-123">Values of the xsd:string type.</span></span>  <br/> |
   

