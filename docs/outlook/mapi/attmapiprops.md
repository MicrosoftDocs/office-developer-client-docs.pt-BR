---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 185bfbb151c4f8d4e36b40b94393d14d50c33edf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410452"
---
# <a name="attmapiprops"></a><span data-ttu-id="b2b0e-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="b2b0e-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="b2b0e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2b0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2b0e-105">O **atributo attMAPIProps** é especial porque pode ser usado para codificar qualquer propriedade MAPI que não tenha uma contraparte no conjunto de atributos definidos por TNEF existentes.</span><span class="sxs-lookup"><span data-stu-id="b2b0e-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="b2b0e-106">Os dados do atributo são um conjunto contado de propriedades MAPI colocadas de ponta a ponta.</span><span class="sxs-lookup"><span data-stu-id="b2b0e-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="b2b0e-107">O formato dessa codificação, que permite qualquer conjunto de propriedades MAPI, é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b2b0e-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="b2b0e-108">_Property_Seq:_</span><span class="sxs-lookup"><span data-stu-id="b2b0e-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="b2b0e-109">contagem de  _Property_Value,..._</span><span class="sxs-lookup"><span data-stu-id="b2b0e-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="b2b0e-110">Deve haver tantas  _Property_Value_ itens como o valor de contagem de propriedades indica.</span><span class="sxs-lookup"><span data-stu-id="b2b0e-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="b2b0e-111">_Property_Value:_</span><span class="sxs-lookup"><span data-stu-id="b2b0e-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="b2b0e-112">propriedade-tag _Property_property-tag  _Proptag_Name Property_</span><span class="sxs-lookup"><span data-stu-id="b2b0e-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="b2b0e-113">A marca de propriedade é simplesmente o valor associado ao identificador da propriedade, como 0x0037001F para **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b2b0e-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="b2b0e-114">_Propriedade:_</span><span class="sxs-lookup"><span data-stu-id="b2b0e-114">_Property:_</span></span>
  
>  <span data-ttu-id="b2b0e-115">_Valor_ de contagem de  _valor,..._</span><span class="sxs-lookup"><span data-stu-id="b2b0e-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="b2b0e-116">_Valor:_</span><span class="sxs-lookup"><span data-stu-id="b2b0e-116">_Value:_</span></span>
  
> <span data-ttu-id="b2b0e-117">value-data value-size value-data padding value-size value-IID value-data padding</span><span class="sxs-lookup"><span data-stu-id="b2b0e-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="b2b0e-118">_Proptag_Name:_</span><span class="sxs-lookup"><span data-stu-id="b2b0e-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="b2b0e-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span><span class="sxs-lookup"><span data-stu-id="b2b0e-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="b2b0e-120">O encapsulamento de cada propriedade varia com base no identificador da propriedade e no tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b2b0e-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="b2b0e-121">Marcas de propriedade, identificadores e tipos são definidos nos arquivos de título Mapitags.h e Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="b2b0e-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="b2b0e-122">Se a propriedade for uma propriedade nomeada, a marca da propriedade será imediatamente seguida pelo nome da propriedade MAPI, consistindo em um identificador global exclusivo (GUID), um tipo e um identificador ou uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="b2b0e-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="b2b0e-123">Propriedades e propriedades de valores múltiplos com valores de comprimento variável, como os tipos de propriedade PT_BINARY, PT_STRING8, PT_UNICODE ou PT_OBJECT, são tratadas da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="b2b0e-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="b2b0e-124">Primeiro, o número de valores, codificados como um longo sem sinal de 32 bits, é colocado no fluxo TNEF, seguido pelos valores individuais.</span><span class="sxs-lookup"><span data-stu-id="b2b0e-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="b2b0e-125">Os dados de valor de cada propriedade são codificados como seu tamanho em bytes seguidos pelos dados de valor em si.</span><span class="sxs-lookup"><span data-stu-id="b2b0e-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="b2b0e-126">Os dados de valor são adicionados a um limite de 4 byte, embora a quantidade de preenchimento não seja incluída no tamanho do valor.</span><span class="sxs-lookup"><span data-stu-id="b2b0e-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="b2b0e-127">Se a propriedade for do tipo PT_OBJECT, o tamanho do valor será seguido pelo identificador da interface do objeto.</span><span class="sxs-lookup"><span data-stu-id="b2b0e-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="b2b0e-128">A implementação atual do TNEF suporta apenas os identificadores IID_IMessage, IID_IStorage e IID_Istream interface.</span><span class="sxs-lookup"><span data-stu-id="b2b0e-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="b2b0e-129">O tamanho do identificador da interface está incluído no tamanho do valor.</span><span class="sxs-lookup"><span data-stu-id="b2b0e-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="b2b0e-130">Se o objeto for uma mensagem incorporada (ou seja, se ele tiver um tipo de propriedade de PT_OBJECT e um identificador de interface de IID_Imessage), os dados de valor serão codificados como um fluxo TNEF incorporado.</span><span class="sxs-lookup"><span data-stu-id="b2b0e-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="b2b0e-131">A codificação real de uma mensagem incorporada na implementação do TNEF é feita abrindo um segundo objeto TNEF para o fluxo original e processando o fluxo embutido.</span><span class="sxs-lookup"><span data-stu-id="b2b0e-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

