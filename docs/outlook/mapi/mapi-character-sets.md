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
ms.openlocfilehash: 898883d8c93b69762883a502b7a4313b3417d0d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319072"
---
# <a name="mapi-character-sets"></a><span data-ttu-id="c354d-103">Conjuntos de caracteres MAPI</span><span class="sxs-lookup"><span data-stu-id="c354d-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="c354d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c354d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c354d-105">Os aplicativos cliente compatíveis com MAPI e provedores de serviços podem usar caracteres ANSI (byte único) ou caracteres Unicode (byte duplo).</span><span class="sxs-lookup"><span data-stu-id="c354d-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="c354d-106">Não há suporte para conjuntos de caracteres OEM.</span><span class="sxs-lookup"><span data-stu-id="c354d-106">OEM character sets are not supported.</span></span> <span data-ttu-id="c354d-107">Uma cadeia de caracteres OEM passada para um método ou função MAPI causará falha no método ou na função.</span><span class="sxs-lookup"><span data-stu-id="c354d-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="c354d-108">Os aplicativos cliente que funcionam com nomes de fileno conjunto de caracteres OEM devem ser cuidadoso para convertê-los em ANSI antes de passá-los para um método ou função MAPI.</span><span class="sxs-lookup"><span data-stu-id="c354d-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="c354d-109">O suporte ao conjunto de caracteres Unicode é opcional, tanto para clientes quanto para provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="c354d-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="c354d-110">Todos os provedores de serviços devem gravar seu código para que eles possam compilar independentemente de terem ou não suporte Unicode.</span><span class="sxs-lookup"><span data-stu-id="c354d-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="c354d-111">Os clientes são compilados condicionalmente, dependendo do nível de suporte, mas os provedores de serviços não.</span><span class="sxs-lookup"><span data-stu-id="c354d-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="c354d-112">Eles não devem ter que ser recompilados quando o conjunto de caracteres é alterado.</span><span class="sxs-lookup"><span data-stu-id="c354d-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="c354d-113">Nada no código do provedor de serviços deve ser condicional.</span><span class="sxs-lookup"><span data-stu-id="c354d-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="c354d-114">Quando clientes ou provedores de serviço que oferecem suporte a Unicode fazem uma chamada de método que inclui cadeias de caracteres como parâmetros de entrada ou saída, eles definem o sinalizador MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="c354d-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="c354d-115">A definição desse sinalizador indica a implementação de que todas as cadeias de caracteres de entrada são cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c354d-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="c354d-116">Na saída, a definição desse sinalizador solicita que todas as cadeias de caracteres passadas da implementação devem ser cadeias de caracteres Unicode, se possível.</span><span class="sxs-lookup"><span data-stu-id="c354d-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="c354d-117">Implementadores de métodos que dão suporte a Unicode serão compatíveis com a solicitação; os implementadores de métodos que não oferecem suporte a Unicode não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="c354d-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="c354d-118">As propriedades de cadeia de caracteres que não estão no formato Unicode são do tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="c354d-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="c354d-119">MAPI define a constante **fMapiUnicode** no arquivo de cabeçalho MAPIDEFS. H para representar o conjunto de caracteres padrão.</span><span class="sxs-lookup"><span data-stu-id="c354d-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="c354d-120">Se um cliente ou provedor de serviços oferecer suporte a Unicode, **fMapiUnicode** é definido como MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="c354d-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="c354d-121">Clientes e provedores de serviço que não dão suporte a Unicode Set **fMapiUnicode** como zero.</span><span class="sxs-lookup"><span data-stu-id="c354d-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="c354d-122">Os provedores de serviços que não dão suporte ao Unicode devem:</span><span class="sxs-lookup"><span data-stu-id="c354d-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="c354d-123">Recusar a execução de conversões entre conjuntos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c354d-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="c354d-124">Nunca passe o sinalizador MAPI_UNICODE em chamadas de método.</span><span class="sxs-lookup"><span data-stu-id="c354d-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="c354d-125">Retornar MAPI_E_BAD_CHARWIDTH quando o sinalizador MAPI_UNICODE for passado.</span><span class="sxs-lookup"><span data-stu-id="c354d-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="c354d-126">Declare explicitamente as propriedades da cadeia de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="c354d-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="c354d-127">Os provedores de serviços também podem retornar MAPI_E_BAD_CHARWIDTH quando só dão suporte a Unicode e clientes não passam o sinalizador MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="c354d-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="c354d-128">A versão atual do MAPI oferece suporte a Unicode nos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="c354d-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="c354d-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="c354d-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="c354d-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="c354d-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="c354d-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="c354d-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="c354d-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="c354d-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="c354d-133">[IMAPIProp:: GetLastError](imapiprop-getlasterror.md) (Apenas implementação do**IAddrBook** )</span><span class="sxs-lookup"><span data-stu-id="c354d-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="c354d-134">Para esses métodos, os chamadores podem esperar que qualquer cadeia de caracteres retornada seja cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c354d-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="c354d-135">As cadeias de caracteres retornadas de implementações MAPI de qualquer outro método serão cadeias de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="c354d-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

