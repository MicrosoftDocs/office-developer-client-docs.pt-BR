---
title: Copiando propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2f9ee7221f523d7c92d91746f5cd719fad821a27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766334"
---
# <a name="copying-mapi-properties"></a><span data-ttu-id="c062f-103">Copiando propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c062f-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="c062f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c062f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c062f-105">Clientes e provedores de serviços podem copiar uma ou mais das propriedades de um objeto com os seguintes métodos **IMAPIProp** e funções da API:</span><span class="sxs-lookup"><span data-stu-id="c062f-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="c062f-106">O método [IMAPIProp::CopyTo](imapiprop-copyto.md) copia todas as propriedades de um objeto para outro objeto, opcionalmente, excluindo propriedades selecionadas.</span><span class="sxs-lookup"><span data-stu-id="c062f-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="c062f-107">**CopyTo** é usado para copiar ou mover qualquer tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="c062f-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="c062f-108">O método [IMAPIProp::CopyProps](imapiprop-copyprops.md) copia propriedades selecionadas de um objeto.</span><span class="sxs-lookup"><span data-stu-id="c062f-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="c062f-109">**CopyProps** é usado principalmente com mensagens.</span><span class="sxs-lookup"><span data-stu-id="c062f-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="c062f-110">Quando um cliente cria uma cópia encaminhada de uma mensagem ou uma resposta, alças **CopyProps** copiando as propriedades adequadas a partir da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="c062f-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="c062f-111">A função [PropCopyMore](propcopymore.md) copia um valor de propriedade exclusivo de um local para outro.</span><span class="sxs-lookup"><span data-stu-id="c062f-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="c062f-112">Use **PropCopyMore** com cautela.</span><span class="sxs-lookup"><span data-stu-id="c062f-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="c062f-113">É possível — ao copiar um valor ao mesmo tempo — alocar muitos pequenos blocos de memória e fazer com que a memória para fragmentar.</span><span class="sxs-lookup"><span data-stu-id="c062f-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="c062f-114">A função [ScCopyProps](sccopyprops.md) copia os valores de propriedade em massa.</span><span class="sxs-lookup"><span data-stu-id="c062f-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="c062f-115">**ScCopyProps** pode copiar os valores de propriedade que foram desenvolvidos de blocos não contíguos de memória.</span><span class="sxs-lookup"><span data-stu-id="c062f-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="c062f-116">Ele retorna uma nova matriz de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c062f-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="c062f-117">Se a matriz de propriedade retornada por **ScCopyProps** deve ser armazenado em disco, use a função [ScRelocProps](screlocprops.md) para ajustar os ponteiros.</span><span class="sxs-lookup"><span data-stu-id="c062f-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="c062f-118">**ScRelocProps** deve ser chamado duas vezes; uma vez para ajustar os endereços antes de gravar a operação de dados e, em seguida, novamente durante a operação de leitura.</span><span class="sxs-lookup"><span data-stu-id="c062f-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="c062f-119">A função **ScRelocProps** pressupõe que a matriz de valores de propriedade foi originalmente alocado em uma única alocação.</span><span class="sxs-lookup"><span data-stu-id="c062f-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="c062f-120">As funções da API descritas as propriedades de cópia lista anterior na memória, em vez de um objeto para outro objeto.</span><span class="sxs-lookup"><span data-stu-id="c062f-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="c062f-121">Essas funções são suportadas atualmente, mas não podem ser suportadas em uma versão futura.</span><span class="sxs-lookup"><span data-stu-id="c062f-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c062f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c062f-122">See also</span></span>



[<span data-ttu-id="c062f-123">Visão geral da propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="c062f-123">MAPI Property Overview</span></span>](mapi-property-overview.md)

