---
title: Conjuntos de caracteres MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5f7da3da8d23b28e13c39570b8f5971cb75a3310
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582529"
---
# <a name="mapi-character-sets"></a><span data-ttu-id="d65c6-103">Conjuntos de caracteres MAPI</span><span class="sxs-lookup"><span data-stu-id="d65c6-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="d65c6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d65c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d65c6-105">Provedores de serviços e aplicativos cliente compatíveis com MAPI podem usar caracteres ANSI (byte único) ou caracteres Unicode (byte duplo).</span><span class="sxs-lookup"><span data-stu-id="d65c6-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="d65c6-106">Não há suporte para conjuntos de caracteres OEM.</span><span class="sxs-lookup"><span data-stu-id="d65c6-106">OEM character sets are not supported.</span></span> <span data-ttu-id="d65c6-107">Uma cadeia de OEM passado a um método MAPI ou função fará com que esse método ou função falha.</span><span class="sxs-lookup"><span data-stu-id="d65c6-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="d65c6-108">Aplicativos de cliente que funcionam com nomes de arquivo no conjunto de caracteres OEM devem tomar cuidadosos convertê-los para ANSI antes de passá-los para uma função ou um método MAPI.</span><span class="sxs-lookup"><span data-stu-id="d65c6-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="d65c6-109">Conjunto de caracteres com suporte o Unicode é opcional, tanto para clientes e provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="d65c6-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="d65c6-110">Todos os provedores de serviço devem escrever seu código para que eles podem compilar independentemente de estarem ou não eles oferecem suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="d65c6-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="d65c6-111">Clientes Compilar condicionalmente, dependendo do seu nível de suporte, mas não provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="d65c6-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="d65c6-112">Eles não precisará ser recompilado quando o conjunto de caracteres alterações.</span><span class="sxs-lookup"><span data-stu-id="d65c6-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="d65c6-113">Nada no código do provedor de serviço deve ser condicional.</span><span class="sxs-lookup"><span data-stu-id="d65c6-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="d65c6-114">Quando clientes ou provedores de serviço que oferecem suporte a Unicode fazer uma chamada de método que inclui as sequências de caracteres como parâmetros de entrada ou saídas, eles definido o sinalizador MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d65c6-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="d65c6-115">Defina esse sinalizador indica feitas na implementação, que todas as cadeias de caracteres de entrada são cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="d65c6-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="d65c6-116">Na saída, definir este sinalizador solicitações que todas as cadeias de caracteres passadas de volta a partir da implementação deve ser cadeias de caracteres Unicode se possível.</span><span class="sxs-lookup"><span data-stu-id="d65c6-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="d65c6-117">Implementadores de método que ofereça suporte a Unicode cumprirá a solicitação; não estejam em conformidade implementadores de método que não oferecem suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="d65c6-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="d65c6-118">Propriedades de cadeia de caracteres que não estão no formato Unicode são do tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="d65c6-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="d65c6-119">MAPI define a constante **fMapiUnicode** no arquivo de cabeçalho MAPIDEFS. H para representar o conjunto de caracteres padrão.</span><span class="sxs-lookup"><span data-stu-id="d65c6-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="d65c6-120">Se um cliente ou serviço provedor oferece suporte a Unicode, **fMapiUnicode** é definido como MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d65c6-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="d65c6-121">Clientes e provedores de serviços que não oferecem suporte a Unicode defina **fMapiUnicode** como zero.</span><span class="sxs-lookup"><span data-stu-id="d65c6-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="d65c6-122">Provedores de serviços que não oferecem suporte a Unicode devem:</span><span class="sxs-lookup"><span data-stu-id="d65c6-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="d65c6-123">Recuse executar conversões entre conjuntos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d65c6-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="d65c6-124">Nunca passe o sinalizador MAPI_UNICODE em chamadas de método.</span><span class="sxs-lookup"><span data-stu-id="d65c6-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="d65c6-125">Retorne MAPI_E_BAD_CHARWIDTH quando o sinalizador MAPI_UNICODE é passado.</span><span class="sxs-lookup"><span data-stu-id="d65c6-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="d65c6-126">Declare explicitamente o propriedades de cadeia de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="d65c6-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="d65c6-127">Provedores de serviços também podem retornar MAPI_E_BAD_CHARWIDTH quando eles só oferecem suporte a Unicode e os clientes não passar o sinalizador MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d65c6-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="d65c6-128">A versão atual do MAPI oferece suporte a Unicode nos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="d65c6-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="d65c6-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="d65c6-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="d65c6-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="d65c6-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="d65c6-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="d65c6-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="d65c6-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="d65c6-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="d65c6-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (Somente para a implementação**IAddrBook** )</span><span class="sxs-lookup"><span data-stu-id="d65c6-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="d65c6-134">Para esses métodos, os chamadores podem esperar qualquer cadeia de caracteres retornada como sequências de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="d65c6-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="d65c6-135">Cadeias de caracteres retornadas de implementações de MAPI de qualquer outro método será cadeias de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="d65c6-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

